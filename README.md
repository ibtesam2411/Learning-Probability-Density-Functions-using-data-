This project focuses on learning probability density functions using a roll-number-parameterized nonlinear model applied to the India Air Quality Data dataset from Kaggle, where NO2 values are used as the feature 
𝑥
x. Each value is transformed using the function 
𝑧
=
𝑥
+
𝑎
𝑟
sin
⁡
(
𝑏
𝑟
𝑥
)
z=x+a
r
	​

sin(b
r
	​

x), where 
𝑎
𝑟
=
0.05
×
(
𝑟
 
m
o
d
 
7
)
a
r
	​

=0.05×(rmod7) and 
𝑏
𝑟
=
0.3
×
(
(
𝑟
 
m
o
d
 
5
)
+
1
)
b
r
	​

=0.3×((rmod5)+1), with roll number 
𝑟
=
102303316
r=102303316, giving 
𝑎
𝑟
=
0.30
a
r
	​

=0.30 and 
𝑏
𝑟
=
0.60
b
r
	​

=0.60. After loading the dataset, cleaning column names, and removing missing values, the transformed variable 
𝑧
z is generated and used to learn parameters of the probability density model 
𝑝
^
(
𝑧
)
=
𝑐
𝑒
−
𝜆
(
𝑧
−
𝜇
)
2
p
^
	​

(z)=ce
−λ(z−μ)
2
. The parameters are estimated using maximum likelihood estimation by computing the mean 
𝜇
μ, variance 
𝜎
2
σ
2
, and deriving 
𝜆
=
1
/
(
2
𝜎
2
)
λ=1/(2σ
2
) and 
𝑐
=
1
/
2
𝜋
𝜎
2
c=1/
2πσ
2
	​

. The implementation is done in Python using pandas, numpy, and matplotlib, and outputs the learned values of 
𝜇
μ, 
𝜆
λ, and 
𝑐
c, along with a visualization comparing the histogram of transformed data to the learned PDF curve. This approach demonstrates how nonlinear transformations and statistical estimation techniques can be used to model real-world environmental data distributions effectively.
