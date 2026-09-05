#Arithmetic operators 

a=10
b=5
print("Addition=",a+b)
print("Subtraction=",a-b)
print("Multiplication=",a*b)
print("Divison=",a/b)
print("Floor division=",a//b)
print("Modulus=",a%b)
print("Exponent=",a**b)

# comparision operators

a=20
b=30
print (a==b)
print(a!=b)
print(a>b)
print(a<b)
print(a<=b)
print(a>=b)


#logical operators

a=10
b=20
print(a>b and a<b)
print(a>=b or a<b)
print(not(a>b))
print(not(a<b))
print(a<=b or a>=b)


#Bitwise Operators

a=12
b=13
print(a&b)
print(a|b)
print(a^b)
print(a>>b)
print(a<<b)



#Membership Operators
#IN
a=[10,20,30,40,50]

print(20 in a)
print(70 in a)

#NOT IN

fruits=["mango","apple","Strawberry","banana"]
print("pineapple" not in fruits)
print("mango" not in fruits)

# Identity OPerators
#IS
a=[10,20,30]
b=[10,20,30]
print(a is b)
print(b is a)

a=10
b=a
print(a is b)
print(a is not b)

#IS NOT
a=[10,20,30]
b=[10,20,25]
print(a is not b)


#Calculator Program
num1=eval(input("Enter first no:"))
num2=eval(input("Enter second no:"))
print("Addition=",num1+num2)
print("Subtraction=",num1-num2)
print("Multiplication=",num1*num2)
print("Divison=",num1/num2)