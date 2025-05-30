Here’s the LaTeX extraction of the text with mathematical expressions properly formatted:

---

**5. Overlap between moving gaussians
We have learned (homework) that the overlap  
$$  
\int dx \, \Psi_1^* \Psi_2  
$$
between two different wave packets $\Psi_1$ and $\Psi_2$ is, on general grounds, time \textit{independent}.  

The following EXAMPLE seems to be in tension with this fact: Consider two gaussians that coincide at $t = 0$ but are moving in opposite directions with large momenta compared to their momenta uncertainties. Now we make two claims:  
1. At $t = 0$ the overlap is big.  
2. Once the centers of the packets are separated by a small multiple of the position uncertainty the overlap is small.  

The purpose of this problem is to find a flaw in the claims of the EXAMPLE.  

Consider a free particle and a normalized gaussian wavepacket $\hat{\Psi}$ at zero time:  
$$  
\hat{\Psi}(x, 0) = \frac{1}{(2\pi)^{1/4} \sqrt{a}} \exp\left(-\frac{x^2}{4a^2}\right).  
$$  

From this we create two wavepackets $\Psi_1$ and $\Psi_2$:  
$$  
\Psi_1(x, 0) \equiv e^{iqx/\hbar} \, \hat{\Psi}(x, 0),  
$$  
$$  
\Psi_2(x, 0) \equiv e^{-iqx/\hbar} \, \hat{\Psi}(x, 0).  
$$  

Here $q$ is a real quantity with units of momentum.  

**(a)** What is $\langle p \rangle$ for $\hat{\Psi}(x, 0)$? Will this expectation value change in time? Explain.  

**(b)** What is $\langle p \rangle$ for $\Psi_1(x, 0)$? What is $\langle p \rangle$ for $\Psi_2(x, 0)$? Do these expectation values change in time?  

**(c)** Compute the zero-time overlap $\gamma(0)$ of the two packets:  
$$  
\gamma(0) = \int \Psi_1^*(x, 0) \Psi_2(x, 0) \, dx.  
$$  
The following integral may be useful:  
$$  
\int_{-\infty}^{\infty} e^{-a x^2 + b x} \, dx = \sqrt{\frac{\pi}{a}} \exp\left(\frac{b^2}{4a}\right), \quad \text{when } \operatorname{Re}(a) > 0.  
$$  

**(d)** Write an inequality that expresses the fact that the momentum of the wavepackets is *large* compared to the momentum uncertainty. What was wrong with the claims of the EXAMPLE?  
