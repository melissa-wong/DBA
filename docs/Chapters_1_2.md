---
output:
  html_document: default
  pdf_document: default
---
# Book Organization

- Introduction to the book.
- No exercises or examples.

# Introduction

- Concept of combining prior and posterior beliefs
- Three goals of inference:
    - Parameter Estimation
    - Prediction
    - Model Comparison
- Introduction to R

## Exercise 2.1

Since there is no way to see or feel the angels, there is no data which can be collected that can alter the belief.  Conversely, it is possible to measure the number of dancing anglers and this is data which could be used to alter the belief.

## Exercise 2.2

<table>
 <thead>
  <tr>
   <th style="text-align:right;"> x </th>
   <th style="text-align:right;"> p(x)=1/4 </th>
   <th style="text-align:right;"> p(x)=x/10 </th>
   <th style="text-align:right;"> p(x)=25/2x </th>
  </tr>
 </thead>
<tbody>
  <tr>
   <td style="text-align:right;"> 1 </td>
   <td style="text-align:right;"> 0.25 </td>
   <td style="text-align:right;"> 0.1 </td>
   <td style="text-align:right;"> 0.48 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 2 </td>
   <td style="text-align:right;"> 0.25 </td>
   <td style="text-align:right;"> 0.2 </td>
   <td style="text-align:right;"> 0.24 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 3 </td>
   <td style="text-align:right;"> 0.25 </td>
   <td style="text-align:right;"> 0.3 </td>
   <td style="text-align:right;"> 0.16 </td>
  </tr>
  <tr>
   <td style="text-align:right;"> 4 </td>
   <td style="text-align:right;"> 0.25 </td>
   <td style="text-align:right;"> 0.4 </td>
   <td style="text-align:right;"> 0.12 </td>
  </tr>
</tbody>
</table>

## Exercise 2.3

After #1's=#2's=#3's=#4's=25, Model A is more likely.

After #1's=48, #2's=24, #3's=16 and #4's=12, Model C is more likely.

## Exercise 2.4

Install R.

## Excerise 2.5


```r
x <- seq(-2, 2, 0.1)
y = x^2
ggplot()+
  geom_line(mapping=aes(x=x, y=y))
```

<img src="Chapters_1_2_files/figure-html/unnamed-chunk-2-1.png" width="672" />

## Exercise 2.6


```r
x <- seq(-3, 3, 0.1)
y = x^3
ggplot()+
  geom_line(mapping=aes(x=x, y=y))
```

<img src="Chapters_1_2_files/figure-html/unnamed-chunk-3-1.png" width="672" />


