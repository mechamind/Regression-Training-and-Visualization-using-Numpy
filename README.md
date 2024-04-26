# Third Order Polynomial Regression Training and Visualization using Numpy
This Python script demonstrates 3rd order polynomial regression using Matplotlib in a Jupyter Notebook. Here's what the script does:
- Generates random noisy data based on a sine wave.
- Performs polynomial regression to fit a 3rd order polynomial curve to the data.
- Shows the derivation of the equations used in the regression.
- Displays the regression curve as an animation in the notebook.

## Animation
[![Watch the Training Animation]](https://youtu.be/pC4bMzm5Qto)


## Requirements
Ensure you have Python installed on your system.
pip install -r requirements.txt

## Theory
Loss Function
$
L = \frac{1}{N} \sum_{i=1}^{N} (y_{\text{pred}_i} - y_i)^2\newline
$


Gradient Calculation
$
\frac{\partial L}{\partial y_{\text{pred}}} = \frac{2}{N} \sum_{i=1}^{N} (y_{\text{pred}_i} - y_i)\newline
$
$\frac{\partial L}{\partial a} = \frac{\partial L}{\partial y_{\text{pred}}} \times \frac{\partial y_{\text{pred}}}{\partial a} = \frac{2}{N} \sum_{i=1}^{N} (y_{\text{pred}_i} - y_i)\newline
$
$
\frac{\partial L}{\partial b} = \frac{\partial L}{\partial y_{\text{pred}}} \times \frac{\partial y_{\text{pred}}}{\partial b} = \frac{2}{N} \sum_{i=1}^{N} (y_{\text{pred}_i} - y_i) \cdot x_i\newline
$
$
\frac{\partial L}{\partial c} = \frac{\partial L}{\partial y_{\text{pred}}} \times \frac{\partial y_{\text{pred}}}{\partial c} = \frac{2}{N} \sum_{i=1}^{N} (y_{\text{pred}_i} - y_i) \cdot x_i^2\newline
$
$
\frac{\partial L}{\partial d} = \frac{\partial L}{\partial y_{\text{pred}}} \times \frac{\partial y_{\text{pred}}}{\partial c} = \frac{2}{N} \sum_{i=1}^{N} (y_{\text{pred}_i} - y_i) \cdot x_i^3\newline
$
$
\text{Updateing} ~a, ~b, ~c ~\text{and} ~d\newline
a \mathrel{-}= \text{learning\_rate} \times \frac{\partial L}{\partial a}\newline
$
$
b \mathrel{-}= \text{learning\_rate} \times \frac{\partial L}{\partial b}\newline
$
$
c \mathrel{-}= \text{learning\_rate} \times \frac{\partial L}{\partial c}\newline
$
$
d \mathrel{-}= \text{learning\_rate} \times \frac{\partial L}{\partial d}\newline
$