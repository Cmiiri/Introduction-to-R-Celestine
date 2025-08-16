#Datatypes(numeric,factor,integer,character
#complex character/string,logical/Boolean)

#alt+-means_assigned_to( <- )
#c()used_to_combine_variables

#1.Numeric
numeric <- 10.5
numeric_many <- c(10,11,12.5,100)

#integer_does_not_have_decimals
integer <- c(1L,10L)

#complex(imaginary part represented by i)
complexs <- c(9+3i)

#character/strings,use speech marks
characters <- c("hello","world","in")

#to_know_data_type_use_the_funtion class ()

#logical/boolean
#this is TRUE/FALSE
a <- 10
b <- 9
a>b
b>a
a==d

as.numeric ()#for converting type to numeric
as.integer() #for converting to integer

#use ? to ask for help in R

#simple maths

#addition +
# subtraction -
 # division /
  #summarize data summary()
#square root sqrt()
#exponent ^
#multiplication*
#modulus/absoulute %

summary(numeric_many)
?summary
x <- 1+2
y <- 1/3
summary(x,y)
summaryc(1,2,3,4,5,6,)
2^4

#Data_structures
#1.vectors_list of items/variables of the same datatype
# we us c() and separate with a comma
x1 <- c("apples","oranges")
x2 <- c(1,2,3,4,5)
x3 <- 1:5
x4 <- 1.5:1.6
x5 <- 1.5:6.3
x6 <- seq(1.5,6.2,by=0.5)#we have defined the steps
#to know length of vector length()
length(x6)
#we sort to arrange numerically/alphabetically sort()
sort(x6)
sortc(6,8.3,6,9)
sort(x2,decreasing = TRUE)#descending order
sort(x2,increasing=FALSE)#ascending order

#access an item in vector we use square brackets[]
x6[3]#third item in x6

x8 <- 65:1000
x8[500]
#2.lists_contain different data types
#we use ()
x9 <- list("apple","kiwi","banana")
#to know the length of a list we use length
length(x9)
#to access second item
x9[2]
#to check if an item is present we us %in%
apple%in%x9
#add an item we append()

x10 <- append(x9,"mango",after1)#specific position
x11 <- append(x9,"mango")

#to join lists
x12 <- c(x9,x11)

#3.matrices_two dimensional data with rows(horizontal)and columns(vertical)
#we use matrix(),we specify rows with nro and columns with ncol

x13 <- matrix(c(1,2,3,4,5,6),nrow=3,ncol=2)
x14 <- matrix(c(1,2,3,4,5.6))

#combine the matrices
5 %in%x14
#dimension dim(())
dim(x14)
#tocheck number of items inside

length(x14)
x15 <- c(1,2,3,4,5,6)

matrix(x15,nrow = 3,ncol = 2)

matrix(x15,nrow = 3,ncol = 2,byrow = TRUE)

matrix(x15,nrow = 3,ncol = 2,byrow = FALSE)

x16 <- c(1,2,3,4,5,6)

x17 <- c(8,9,10,11,12,13)

#creating matrix using two lists
#Quiz??

#creating a matrix using three vectors

matrix(c(x15,x16,x17),ncol = 3)

#combine three vectors by column, we use cbind()
#the vectors should be of the same length
cbind(x15,x16,x17)

#combine the vectors by row, we use rbind(
#the vectors should be of the same length
rbind(x15,x16,x17)

thismatrix <- rbind(x17,x16,x15)

#to access an item in a matrice we use[]or[c()] for more than one item
thismatrix[1,2]
thismatrix[1,]
thismatrix[,1]
thismatrix[c(1,2)]

#checking if an item is in a matrix we use %in%
12 %in% thismatrix
50 %in% thismatrix

#check the number of rows and number of columns in a matrix,use dim()
dim(thismatrix)

#checking the number of rows and number of columns  in a matrix,we use length()

length(thismatrix)

#4.Arrays
#object can hold multi_dimensional data
#use array()to create and dim()to specify dimension
#elements are of the same data type
#we access elements of an array using[]
#use %in% to check if item is present in an array
#use dim()to check number of rows and columns
#use length()to check dimension

arrays <- c(1:14) #one dimension

arrays_1 <- array(arrays,dim = c(4,3,2) ) #multidimension

#5,Data frames

#two dimensional tabular data that stores data in rows and columns,just like an excel sheet
#can have different data types,but each column should have the same data type
#use data.frame() to create
#use [] or [[]] and $ to access columns of a data frame
#use rbind()to add rows /add data vertically
#and cbind() to add columns/add data horizontally
#use dim() to check number of rows and columns
#use ncol()/length() and nrow( ) to check number of columns or rwos repectively

x18 <- c("a","b","c","d","e","f")


data_frame <- data.frame(x15,x16,x17,x18)

data_frame

summary(data_frame)
