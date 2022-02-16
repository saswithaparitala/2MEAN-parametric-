# 2MEAN-parametric-
x<-c(8260,	8130,	8350,	8070,	8340)
y<-c(7950,	7890,	7900,	8140,	7920,	7840)
#x<-c(59,	68,	44,	71,	63,	46,	69,	54,	48)
#y<-c(50,	36,	62,	52,	70,	41)
print("enter the level of significance")
alpha<-scan()
n1<-length(x)
n2<-length(y)
sd=sqrt((((n1-1)*sd(x)^2)+(n2-1)*sd(y)^2)/(n1+n2-2))
tvalue=(mean(x)-mean(y))/(sd*sqrt((1/n1)+(1/n2)))
print("mean of x:")
print(mean(x))
print("mean of y:")
print(mean(y))
print("Combined SD")
print(sd)
print("Calculated value of t:")
print(round(tvalue,digits=4))
t<-t.test(x,y)
print(t)
print("Table value for two-tailed test:")
tablevalue<-qt(1-alpha/2, df=n1+n2-2)
print(round(tablevalue,digits=3))
print("Table value for one-tailed test:")
tablevalue<-qt(1-alpha, df=n1+n2-2)
print(round(tablevalue,digits=3))


OUTPUT:
 print("enter the level of significance")
[1] "enter the level of significance"
> alpha<-scan()
1: 0.01
 print("mean of x:")
[1] "mean of x:"
> print(mean(x))
[1] 8230
> print("mean of y:")
[1] "mean of y:"
> print(mean(y))
[1] 7940
> print("Combined SD")
[1] "Combined SD"
> print(sd)
[1] 114.3095
> print("Calculated value of t:")
[1] "Calculated value of t:"
> print(round(tvalue,digits=4))
[1] 4.1897
> t<-t.test(x,y)
> print(t)

	Welch Two Sample t-test

data:  x and y
t = 4.1136, df = 7.8588, p-value = 0.003505
alternative hypothesis: true difference in means is not equal to 0
95 percent confidence interval:
 126.9208 453.0792
sample estimates:
mean of x mean of y 
     8230      7940 

> print("Table value for two-tailed test:")
[1] "Table value for two-tailed test:"
> tablevalue<-qt(1-alpha/2, df=n1+n2-2)
> print(round(tablevalue,digits=3))
[1] 3.25
> print("Table value for one-tailed test:")
[1] "Table value for one-tailed test:"
> tablevalue<-qt(1-alpha, df=n1+n2-2)
> print(round(tablevalue,digits=3))
[1] 2.821
