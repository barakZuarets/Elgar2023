1)

def priceCheck( products, productPrices, productSold, soldPrice):
    counter=0
    length = len (productSold)
    for i in range(length):
        temp = products.index(productSold[i])
        if soldPrice[i] !=  productPrices[temp]:
    	    counter = counter +1
    return(counter) 
    
products = ['eggs', 'milk','cheese']
productPrices = [2.89, 3.29, 5.79]
productSold = ['eggs', 'eggs','cheese','milk']
soldPrice = [2.89, 2.99, 5.97, 3.29]

print(priceCheck( products, productPrices, productSold, soldPrice) )

products=['rice', 'sugar', 'wheat', 'cheese']
productPrices=[16.89, 56.92, 20.89, 345.99]
productSold=['rice', 'cheese']
soldPrice=[18.99, 400.89]

print(priceCheck( products, productPrices, productSold, soldPrice) )
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
def summer(num):
    if (num<10):
        return num
    return (num %10 + summer(int(num / 10)))

print(summer(2347623))
4)
int(input("enter a number: "))