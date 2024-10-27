Wir haben 2 Gleichungen
- Die Rekursions-Gleichung
  $(I)f(n)=2f\left(\frac{n}{2}\right)+cn+d$
- Die vermutete Funktionsschar der der Algorithmus zugehörig ist
  $(II)f(n)=\alpha+\beta n+\delta n\log_2{n}$
Behauptung 
$$
\begin{align}
&f(n)=\alpha+\beta n+\delta n\log_2{n}=2f\left(\frac{n}{2}\right)+cn+d
\\
&\text{für }\alpha,\beta,\delta\in\mathbb{R}
\end{align}
$$ 
=> $(II)$ in Behauptung einsetzen (Induktionshypothese)
$$
\begin{align}
f(n)
&=2\left(\alpha+\beta n+\delta \frac{n}{2}\log_2{\frac{n}{2}}\right)+cn+d 
\\
&=2\alpha+2\beta n+2\delta\frac{n}{2}\left(\log_2{n}-\log_2{2}\right)+cn+d
\\
&=2\alpha+d+\left(2\beta-\delta+c\right)n+\delta n\log_2{n}
\end{align}
$$
Koeffizienten vergleich mit $f(n)=\alpha+\beta n+\delta n\log_2{n}$


