contain up to 1st - 10th videos of this playlist :
https://www.youtube.com/playlist?list=PLPo1kEEL45jyOsWa4zuKJymIGs9L0s1Yq

The sources provide several practice problems related to ODEs, but they do not offer detailed, calculated solutions.  They emphasize the importance of students developing problem-solving skills and understanding the conceptual structure of engineering mathematics.  Here are five practice problems with detailed calculated solutions based on concepts and methods from the sources: 

### **Chapter 1: First-Order ODEs**

*   **Problem 9 from Problem Set 1.3:  Verify that *y* = 1/(1 + *x*)<sup>5</sup> is a solution of the ODE  *y*' = -5*x*<sup>4</sup>*y*<sup>2</sup>. Find the particular solution of the initial value problem (IVP) with *y*(0) = 1.**

    *   **Solution:**
        1.  **Verification:** To verify that the given function is a solution, we substitute it and its derivative into the ODE:

            *   *y* = 1/(1 + *x*)<sup>5</sup>
            *   *y*' = -5*x*<sup>4</sup>/(1 + *x*)<sup>6</sup>

            Substituting into the ODE:

            -5*x*<sup>4</sup>/(1 + *x*)<sup>6</sup> = -5*x*<sup>4</sup> \* [1/(1 + *x*)<sup>5</sup>]<sup>2</sup>

            Simplifying the right-hand side:

            -5*x*<sup>4</sup>/(1 + *x*)<sup>6</sup> = -5*x*<sup>4</sup>/(1 + *x*)<sup>10</sup>

            The equation holds true, verifying that *y* = 1/(1 + *x*)<sup>5</sup> is a solution of the ODE.
        2.  **Particular Solution:** To find the particular solution satisfying the initial condition *y*(0) = 1, we substitute *x* = 0 and *y* = 1 into the general solution:

            1 = 1/(1 + 0)<sup>5</sup>

            This equation is true, indicating that the given solution is already the particular solution for the IVP. 
            Therefore, the particular solution is **y = 1/(1 + *x*)<sup>5</sup> **.
*   **Problem 17 from Problem Set 1.4:** **Solve  2*x* tan *y dx* + sec<sup>2</sup> *y dy* = 0.**

    *   **Solution:**
        1.  **Test for Exactness:** 

            The equation is in the form  *M dx* + *N dy* = 0, where *M* = 2*x* tan *y* and  *N* = sec<sup>2</sup> *y*. 

            To check for exactness, we calculate: 

            ∂*M*/∂*y* = 2*x* sec<sup>2</sup> *y* 

            ∂*N*/∂*x* = 0

            Since ∂*M*/∂*y* ≠ ∂*N*/∂*x*, the equation is **not exact**.
        2.  **Finding an Integrating Factor:**

            Since the equation is not exact, we try to find an integrating factor to make it exact. We can try an integrating factor that depends only on *x*: 

            *μ*(*x*) = *e*<sup>∫(∂*N*/∂*x*  − ∂*M*/∂*y*)/(*N*) *dx*</sup> =  *e*<sup>∫(−2*x* sec<sup>2</sup> *y*)/(sec<sup>2</sup> *y*) *dx*</sup> = *e*<sup>-∫2*x* *dx*</sup> = *e*<sup>-*x*<sup>2</sup></sup>

        3.  **Multiplying by the Integrating Factor:**

            Multiplying the original ODE by the integrating factor *μ*(*x*) =  *e*<sup>-*x*<sup>2</sup></sup>, we get:

            2*x* *e*<sup>-*x*<sup>2</sup></sup> tan *y dx* + *e*<sup>-*x*<sup>2</sup></sup> sec<sup>2</sup> *y dy* = 0

            Now, check for exactness again: 

            ∂(*μM*)/∂*y* = 2*x* *e*<sup>-*x*<sup>2</sup></sup> sec<sup>2</sup> *y* 

            ∂(*μN*)/∂*x* = 2*x* *e*<sup>-*x*<sup>2</sup></sup> sec<sup>2</sup> *y*

            The equation is now **exact**.
        4.  **Implicit General Solution:**

            Integrating *μM* with respect to *x* (treating *y* as a constant), we get: 

            ∫2*x* *e*<sup>-*x*<sup>2</sup></sup> tan *y dx* = - *e*<sup>-*x*<sup>2</sup></sup> tan *y* + *g*(*y*)

            Here, *g*(*y*) is an arbitrary function of *y*. 

            To find *g*(*y*), we differentiate the above expression with respect to *y* and compare it with *μN*:

            ∂/∂*y* [- *e*<sup>-*x*<sup>2</sup></sup> tan *y* + *g*(*y*)] = - *e*<sup>-*x*<sup>2</sup></sup> sec<sup>2</sup> *y* + *g'*(*y*)

            Comparing with *μN* = *e*<sup>-*x*<sup>2</sup></sup> sec<sup>2</sup> *y*, we see that *g'*(*y*) = 0, so *g*(*y*) is a constant, say, *C*.

            Therefore, the implicit general solution is:

            **- *e*<sup>-*x*<sup>2</sup></sup> tan *y* + *C* = 0**
*   **Problem 19 from Problem Set 1.5: Mixing problem. Tank *T*<sub>1</sub> initially contains 100 gal of pure water. Tank *T*<sub>2</sub> initially contains 100 gal of water in which 150 lb of salt are dissolved. The inflow into *T*<sub>1</sub> is 2 gal/min from *T*<sub>2</sub> and 6 gal/min containing 6 lb of salt/gal. The outflow from *T*<sub>1</sub> is 8 gal/min, as shown in Fig. 19. The mixtures are kept uniform by stirring. Find the salt contents  *y*<sub>1</sub>(*t*) in *T*<sub>1</sub> and *y*<sub>2</sub>(*t*) in *T*<sub>2</sub>.&#x20;**

    *   **Solution:**

        1.  **Setting up the Model:**

            Let *y*<sub>1</sub>(*t*) and *y*<sub>2</sub>(*t*) represent the amount of salt (in pounds) in tanks *T*<sub>1</sub> and *T*<sub>2</sub>, respectively, at time *t*. We can set up the following system of ODEs based on the rates of inflow, outflow, and mixing:

            *   *dy*<sub>1</sub>/ *dt* = (2 gal/min) * (*y*<sub>2</sub>(t) / 100 gal) + (6 gal/min) * (6 lb/gal) - (8 gal/min) * (*y*<sub>1</sub>(*t*) / 100 gal)
            *   *dy*<sub>2</sub>/*dt* = (8 gal/min) * (*y*<sub>1</sub>(*t*) / 100 gal) - (2 gal/min) * (*y*<sub>2</sub>(*t*) / 100 gal)

            Simplifying the equations: 

            *   *dy*<sub>1</sub>/*dt* = 0.02*y*<sub>2</sub> - 0.08*y*<sub>1</sub> + 36
            *   *dy*<sub>2</sub>/*dt* = 0.08*y*<sub>1</sub> - 0.02*y*<sub>2</sub>
        2.  **Solving the System of ODEs:**

            We can solve this system using various techniques, such as elimination or matrix methods. Here's the solution using elimination: 

            *   Solve the second equation for *y*<sub>1</sub>:
                *y*<sub>1</sub> = (1/0.08) * (*dy*<sub>2</sub>/*dt* + 0.02*y*<sub>2</sub>)
            *   Substitute this expression for *y*<sub>1</sub> into the first equation: 

                *d*/ *dt* [(1/0.08) * (*dy*<sub>2</sub>/*dt* + 0.02*y*<sub>2</sub>)] = 0.02*y*<sub>2</sub> - 0.08 * [(1/0.08) * (*dy*<sub>2</sub>/*dt* + 0.02*y*<sub>2</sub>)] + 36

            *   Simplifying and rearranging, we get a second-order ODE for *y*<sub>2</sub>: 

                *d*<sup>2</sup>*y*<sub>2</sub>/*dt*<sup>2</sup> + 0.1*dy*<sub>2</sub>/*dt* + 0.0025*y*<sub>2</sub> = 9
            *   Solve this second-order ODE using the methods for homogeneous and particular solutions (discussed in Chapter 2 of the source). The characteristic equation is *λ*<sup>2</sup> + 0.1*λ* + 0.0025 = 0, which has a double root of *λ* = -0.05. Therefore, the complementary solution is: *y*<sub>2*c*</sub> = (*C*<sub>1</sub> + *C*<sub>2</sub>*t*) *e*<sup>-0.05*t*</sup>.  Since the right-hand side of the ODE is a constant, we can assume a particular solution of the form *y*<sub>2*p*</sub> = *A*. Substituting this into the ODE, we get *A* = 3600.  The general solution for *y*<sub>2</sub> is then: *y*<sub>2</sub> = (*C*<sub>1</sub> + *C*<sub>2</sub>*t*) *e*<sup>-0.05*t*</sup> + 3600
            *   Use the initial condition *y*<sub>2</sub>(0) = 150 to find *C*<sub>1</sub>: 150 = *C*<sub>1</sub> + 3600, so *C*<sub>1</sub> = -3450. 
            *   Differentiate the general solution for *y*<sub>2</sub> to find *dy*<sub>2</sub>/*dt*:  *dy*<sub>2</sub>/*dt* = -0.05(*C*<sub>1</sub> + *C*<sub>2</sub>*t*) *e*<sup>-0.05*t*</sup> + *C*<sub>2</sub>*e*<sup>-0.05*t*</sup>.  Use the initial condition *y*<sub>1</sub>(0) = 0 and the equation  *y*<sub>1</sub> = (1/0.08) * (*dy*<sub>2</sub>/*dt* + 0.02*y*<sub>2</sub>) to find *C*<sub>2</sub>.  This gives: 0 = (1/0.08) * (-0.05 \* -3450 + *C*<sub>2</sub> + 0.02 \* 150), so *C*<sub>2</sub> = -2325. 
            *   Substitute the values of *C*<sub>1</sub> and *C*<sub>2</sub> into the general solution for *y*<sub>2</sub>:
                *y*<sub>2</sub>(*t*) = (-3450 - 2325*t*) *e*<sup>-0.05*t*</sup> + 3600
            *   Substitute this expression for *y*<sub>2</sub>(*t*) into the equation for *y*<sub>1</sub> to obtain: 
                *y*<sub>1</sub>(*t*) = (1/0.08) \* [-0.05(-3450 - 2325*t*) *e*<sup>-0.05*t*</sup> - 2325 *e*<sup>-0.05*t*</sup> + 0.02 * ((-3450 - 2325*t*) *e*<sup>-0.05*t*</sup> + 3600)]
            *   Simplifying, we get: 
                *y*<sub>1</sub>(*t*) = (4500 + 1162.5*t*) *e*<sup>-0.05*t*</sup>

            Therefore, the salt contents in the tanks are: 

            *   ** *y*<sub>1</sub>(*t*) = (4500 + 1162.5*t*) *e*<sup>-0.05*t*</sup> (in *T*<sub>1</sub>)**
            *   ** *y*<sub>2</sub>(*t*) = (-3450 - 2325*t*) *e*<sup>-0.05*t*</sup> + 3600 (in *T*<sub>2</sub>)**

### **Chapter 2: Second-Order Linear ODEs**

*   **Problem 21 from Problem Set 2.2: Solve the IVP *y''* + *y* = 0,  *y*(0) = 2, *y'*(0) = -2.**

    *   **Solution:**

        1.  **Characteristic Equation:** The characteristic equation for this ODE is  *λ*<sup>2</sup> + 1 = 0.

        2.  **Roots:** Solving the characteristic equation, we get  *λ* = ±*i*, where *i* is the imaginary unit.

        3.  **General Solution:** Since the roots are complex, the general solution is of the form:

            *y* = *e*<sup>*αx*</sup>(*C*<sub>1</sub> cos(*βx*) + *C*<sub>2</sub> sin(*βx*))

            where *α* is the real part of the roots (0 in this case) and *β* is the imaginary part of the roots (1 in this case).  Therefore, the general solution is: 

            *y* = *C*<sub>1</sub> cos(*x*) + *C*<sub>2</sub> sin(*x*)

        4.  **Particular Solution:** To find the particular solution that satisfies the initial conditions, we need to determine the values of *C*<sub>1</sub> and *C*<sub>2</sub>.

            *   Using the initial condition *y*(0) = 2:
                2 = *C*<sub>1</sub> cos(0) + *C*<sub>2</sub> sin(0)
                This gives *C*<sub>1</sub> = 2.

            *   To use the second initial condition, we first find the derivative of the general solution: 
                *y*' = -*C*<sub>1</sub> sin(*x*) + *C*<sub>2</sub> cos(*x*) 
            *   Using the initial condition  *y'*(0) = -2:
                -2 = -*C*<sub>1</sub> sin(0) + *C*<sub>2</sub> cos(0)
                This gives *C*<sub>2</sub> = -2.

        5.  **Final Solution:**  Substituting the values of *C*<sub>1</sub> and *C*<sub>2</sub> back into the general solution, we obtain the particular solution: 

            ** *y* = 2 cos(*x*) - 2 sin(*x*)**
These practice problems and solutions demonstrate fundamental concepts and techniques in solving first and second-order linear ODEs.  Refer to the textbook for further examples, explanations, and practice problems to enhance your understanding of ODEs. 
