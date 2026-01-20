# Assignment_Advance-Mathematics

Assignment 1:
Estimation of a Probability Density Function Using Roll-Number-Dependent Non-Linear Data Transformation

Overview:

This assignment demonstrates the process of learning a Probability Density Function (PDF) from real-world environmental data. A customized non-linear transformation, derived from the student’s roll number, is applied to the input data before estimating the probability distribution. The goal is to understand how transformations affect data distribution and how PDFs can be learned from observed samples.

Dataset Information:

Dataset Source: India Air Quality Dataset
Selected Feature: NO₂ (Nitrogen Dioxide concentration)
Nature of Data: Continuous numerical values
The NO₂ attribute is chosen because it is appropriate for modeling continuous probability distributions.

Steps:

Step 1: Data Cleaning and Preparation
The air quality dataset is imported using Pandas.
Invalid, missing, or non-numeric values in the NO₂ column are removed.
The cleaned NO₂ values are stored as the variable x for further processing.

Step 2: Roll-Number-Based Non-Linear Mapping
Each data point x is transformed into a new variable z using a non-linear function defined as:

𝑧=𝑥+𝑎𝑟⋅sin(𝑏𝑟⋅𝑥)
where:
𝑎𝑟=0.05×(𝑟 mod 7)ar=0.05×(rmod7)
𝑏𝑟=0.3×((𝑟 mod5)+1)br=0.3×((rmod5)+1)
r represents the university roll number

This step introduces controlled non-linearity and ensures that the transformation is unique for each student.

Step 3: Probability Density Modeling
The transformed data z is modeled using a Gaussian-like probability density function:
p​(z)=c⋅e−λ(z−μ)2
where:
μ is the mean of the transformed data
λ determines the dispersion
c is the normalization constant

Step 4: Estimation of Parameters
Statistical techniques are used to compute:
The mean (μ)
The spread parameter (λ)
The normalization constant (c)
These parameters fully describe the learned probability density function.

Analysis and Visual Interpretation:

Distribution Histogram
The histogram of the transformed variable z shows a smooth and continuous distribution, suitable for density estimation.
PDF Overlay
The estimated probability density curve aligns well with the histogram, indicating an accurate parameter estimation.
Impact of Transformation
The roll-number-based transformation slightly modifies the original data distribution while maintaining its probabilistic structure.

Observations:

The transformation introduces personalization without distorting the data excessively.
The resulting distribution closely resembles a Gaussian shape.
The learned PDF effectively captures the behavior of the transformed data.
Graphical plots validate the correctness of the estimation.

Technologies Used:

Python
NumPy
Pandas
Matplotlib

Learning Outcomes:

Gaining intuition about Probability Density Functions
Applying non-linear transformations to real data
Estimating PDF parameters from samples
Analyzing distributions through visualization



Name: Vriti Marwaha
Roll Number: 102313063
Lecture Group: L3
