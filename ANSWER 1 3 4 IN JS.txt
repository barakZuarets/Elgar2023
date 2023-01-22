1)
function priceCheck( products = [], productPrices = [], productSold = [], soldPrice = [])
{
	let counter=0;
	for (let i=0;i< productSold.length; i++)
    {
    	let temp = products.indexOf(productSold[i]);
    	if (soldPrice[i] !=  productPrices[temp])
        {
        	counter ++;
        }
    }
    return counter;
}

let products = ["eggs", "milk","cheese"]
let productPrices = [2.89, 3.29, 5.79]
let productSold = ["eggs", "eggs","cheese","milk"]
let soldPrice = [2.89, 2.99, 5.97, 3.29]

console.log(priceCheck(products,productPrices,productSold,soldPrice));
products=["rice", "sugar", "wheat", "cheese"]
productPrices=[16.89, 56.92, 20.89, 345.99]
productSold=["rice", "cheese"]
soldPrice=[18.99, 400.89]
console.log(priceCheck(products,productPrices,productSold,soldPrice));

2)
CREATE TABLE EMPLOYEE (
  ID INTEGER PRIMARY KEY,
  NAME TEXT NOT NULL,
  DEPT_ID INTEGER NOT NULL
);
-- insert some values
INSERT INTO EMPLOYEE VALUES (1, 'Candice', 1);
INSERT INTO EMPLOYEE VALUES (2, 'Julia', 2);
INSERT INTO EMPLOYEE VALUES (3, 'Bob', 4);
INSERT INTO EMPLOYEE VALUES (4, 'Scarlet', 1);
INSERT INTO EMPLOYEE VALUES (5, 'Ileana', 4);

CREATE TABLE DEPARTMENT (
  ID INTEGER PRIMARY KEY,
  NAME TEXT NOT NULL
);
-- insert some values
INSERT INTO DEPARTMENT VALUES (1, 'Executive');
INSERT INTO DEPARTMENT VALUES (2, 'Production');
INSERT INTO DEPARTMENT VALUES (3, 'Resources');
INSERT INTO DEPARTMENT VALUES (4, 'Technical');
INSERT INTO DEPARTMENT VALUES (5, 'Management');
-- fetch some values
SELECT DEPARTMENT.NAME ,COUNT(EMPLOYEE.ID)  FROM DEPARTMENT 
LEFT JOIN EMPLOYEE  ON DEPARTMENT.ID = EMPLOYEE.DEPT_ID
GROUP BY DEPARTMENT.NAME
ORDER BY COUNT(EMPLOYEE.ID) DESC,  DEPARTMENT.NAME ASC;






3)
function summer(num)
{
    if (num<10)
        return num
    return num %10 + summer(parseInt(num / 10) )
}

console.log (summer(2347623))



4)

let temp,max,count;
temp = parseInt (prompt("enter a number: "));
max=0;
count=0;
while (temp != 0)
{
    if (temp > max)
    {
        max=temp;
        count = 1;
    }
    else if (temp == max)
    {
        count++;
    }
    console.log (count)
    temp = parseInt (prompt("enter a number: "));
}

console.log (`sequence maximum is: ${max} and we have ${count} ${max}s in the sequence.`)
