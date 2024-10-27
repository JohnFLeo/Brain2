
![[AUD/Blatt01.pdf#page=1&rect=75,595,528,715|Blatt01, p.1]]

|                        | $n$    | $10^4\cdot n^2$             | $2^n$                                                          | $n!$ |
| ---------------------- | ------ | --------------------------- | -------------------------------------------------------------- | ---- |
| max Eingabe mit $10^5$ | $10^5$ | $\lfloor\sqrt{10}\rfloor=3$ | $\lfloor\log_2{10^5}\rfloor=\lfloor5\cdot\log_2{10}\rfloor=16$ | 8    |
| max Eingabe mit $10^6$ | $10^6$ | $10$                        | $\lfloor\log_2{10^6}\rfloor=\lfloor6\cdot\log_2{10}\rfloor=19$ | 9    |
für $n!$ wird folgendes java Programm genutzt

```java

public static int fac(int n){  
    if(n == 0 || n == 1){  
        return 1;  
    }  
    return n*fac(n-1);  
}  
public static void main(String[] args){  
    while(fac(i) < 1000000){  
        System.out.println("Eingabelänge: "+i+" Rechenschritte "+fac(i));  
        i+=1;  
    }  
    System.out.println("geht nicht mehr->Eingabelänge: "+i+" Rechenschritte "+fac(i));   
}
````
das folgende Ausgabe Erzeugt
```
Eingabelänge: 0 Rechenschritte 1
Eingabelänge: 1 Rechenschritte 1
Eingabelänge: 2 Rechenschritte 2
Eingabelänge: 3 Rechenschritte 6
Eingabelänge: 4 Rechenschritte 24
Eingabelänge: 5 Rechenschritte 120
Eingabelänge: 6 Rechenschritte 720
Eingabelänge: 7 Rechenschritte 5040
Eingabelänge: 8 Rechenschritte 40320
Eingabelänge: 9 Rechenschritte 362880
geht nicht mehr->Eingabelänge: 10 Rechenschritte 3628800
````

![[AUD/Blatt01.pdf#page=1&rect=76,491,533,540|Blatt01, p.1]]
![[AUD/Blatt01.pdf#page=1&rect=76,471,533,495|Blatt01, p.1]]
Zu zeigen:
$$
\exists c>0 \exists n_0>0 \forall n \geq n_0: \log{n^n}\leq c\cdot n\cdot\log{n}
$$
da laut den Logarithmus-Gesetzen gilt $\log{n^n}=n\cdot\log{n}$ 
ist mit $c=1$ und $n_0=1$ die Gleichung korrekt
![[AUD/Blatt01.pdf#page=1&rect=75,447,531,472|Blatt01, p.1]]

$f(n)=\mathcal{O}(g(n))$ bedeutet es gilt $\exists c>0 \exists n_0>0 \forall n \geq n_0: f(n) \leq c \cdot g(n)$ 
Damit die Gleichung erfüllt ist muss gezeigt werden, dass gilt
$$
\begin{align}
\exists c_1>0 \exists n_0>0 \forall n \geq n_0: \log(f(n)) \leq c_1 \cdot \log(g(n))
\end{align}
$$


