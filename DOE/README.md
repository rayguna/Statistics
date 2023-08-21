### Notes on Design of Experiments (DOE)

DOE is a collection of tools and techniques for studying the correlations between multiple input variables. Let's discuss some of these tools.

1. Factors and Levels
   
   - Factors is the number of variable that are being studied.
   
   - Factor Levels refer to the values or settings that a factor can take.  

2. Two-level Full Factorial (2^k)
   
   - Denoted as 2^k design, where 2 refers to the number of levels and k refers to the number of factors.
   
   - For instance, let's consider studing the effect of tire air pressure and driving speed on the fuel efficiency of a car. 
   
   - In this case, the factors are (A) tire air pressure and (B) driving speed. Hence, this scenario translates to a 2^2 design. The fuel efficiency is the (R) response variable. 
   
   - To study the correlation between A and B using a 2^2 full factorial design, we need to select the two levels for each factor. We refer to the two levels as low (-) and high (+). For example, we can set the tire air pressure to (A-) 30 and (A+) 35 psi and set the driving speed to (B-) 35 and (B+) 60 mi/h. Nonetheless, the levels don't have to be numerical. As an example, we can set the tire level to be (A-) winter or (A+) all  season tire.
   
   - The possible combinations of the different factors and levels lead to a total of 2^2=4 as shown in the table below. To perform such an experiment, we record the fuel efficiency for each run to complete the table. Each condition may be repeated or replicated to account for variability in the results. 
   
   - Repeats refer to multiple measurements or observations within a single experimental run. Replicates refer to conducting the entire experiment multiple times.   
     
     | Run | A   | B   | R   |
     | --- | --- | --- | --- |
     | 1   | 30  | 35  |     |
     | 2   | 30  | 60  |     |
     | 3   | 35  | 35  |     |
     | 4   | 35  | 60  |     |
   
   - A full 2^2 design captures the main effects (single-factor interaction) and the two-factor interactions, as follows. Similarly, a full 2^3 design captures up to three-factor interactions and 2^n design captures up to n-factor interactions.
     
     | Run | A   | B   | AB  | R   |
     | --- | --- | --- | --- | --- |
     | 1   | -   | -   | +   |     |
     | 2   | -   | +   | -   |     |
     | 3   | +   | -   | -   |     |
     | 4   | +   | +   | +   |     |

3. Two-level Fractional Factorial, 2^(k-p)
   
   - In some cases, the study involves a large number of variables and the number required experiments become numerous. There may be limited time and resources to perform all possible combination and therefore not feasible. 
   
   - Fractional factorial experiment cut down on the number of experiments by 2^p.   
   
   - For instance, an experiment involving 5 factors will require a total of 2^6 or 64 runs. By employing a 2^(6-1) design, we reduce the total number of runs by half to 32. We can further reduce the total number of runs by employing a 2^(6-2) design to 16. 
   
   - As k increases, however, you will lose information about the interaction between the factors. Moreover, <ins>the choice of selecting the combination of factors and levels that you wish to perform experiments on will determine the number of interaction factors that can be captured</ins>. This is referred to as the resolution.
   
   - For example, a resolution I is the lowest resolution level and can only distinguish between main effects, resolution II can distinguish between main effects and some two-factor interactions, resolution III can additionally distinguish some three-factor interactions, and so on. Please see the table below for an example of a 2III^(7-4) design.
     
     | Run | A   | B   | C   | D=AB | E=AC | F=BC | G=ABC | +       |
     | --- | --- | --- | --- | ---- | ---- | ---- | ----- | ------- |
     | 1   | -   | -   | -   | +    | +    | +    | -     | def     |
     | 2   | +   | -   | -   | -    | -    | +    | +     | afg     |
     | 3   | -   | +   | -   | -    | +    | -    | +     | beg     |
     | 4   | +   | +   | -   | +    | -    | -    | -     | abd     |
     | 5   | -   | -   | +   | +    | -    | -    | +     | cdg     |
     | 6   | +   | -   | +   | -    | +    | -    | -     | ace     |
     | 7   | -   | +   | +   | -    | -    | +    | -     | bcf     |
     | 8   | +   | +   | +   | +    | +    | +    | +     | abcdefg |

4. Mixed-level Factorial
   
   - In some cases, the number of levels for each factor in the study are not the same. This leads to a mixed-level factorial design. 
   
   - For example, a 2^3x3^2 design refers to a three-factor two-levels and two-factor three-levels design. 

5. Plackett-Burman Design
   
   - This design is usually used to study many factors. The design involves a fraction of all possible combination runs. As a result, it can only capture the main effect. It doesn't give information about the interaction between the various factors. 

6. Taguchi Method
   
   - Similar to the Plackett-Burman design, the Taguchi method cut down the number of experiments. However, it can capture both the main and the two-factor interactions.
   
   - This is the case because Taguchi design uses orthogonal arrays, where the experimental runs for any two factors capture all of the four possible combinations (e.g., A+B+, A+B-, A-B+, and A-B- or 11, 12, 21, and 22). See the table below for an example for the L8 orthogonal array. 
   
   - This design is used to study 4 to 7 factors while limiting the number of runs to just 8. A full factorial experiment will otherwise require 16 to 128 runs.
     
     | Run | A   | B   | C   | D   | E   | F   | G   | R   |
     | --- | --- | --- | --- | --- | --- | --- | --- | --- |
     | 1   | 1   | 1   | 1   | 1   | 1   | 1   | 1   |     |
     | 2   | 1   | 1   | 2   | 2   | 2   | 2   | 2   |     |
     | 3   | 1   | 2   | 2   | 1   | 1   | 2   | 2   |     |
     | 4   | 1   | 2   | 2   | 2   | 2   | 1   | 1   |     |
     | 5   | 2   | 1   | 2   | 1   | 2   | 1   | 2   |     |
     | 6   | 2   | 1   | 2   | 2   | 1   | 2   | 1   |     |
     | 7   | 2   | 2   | 1   | 1   | 2   | 2   | 1   |     |
     | 8   | 2   | 2   | 1   | 2   | 1   | 1   | 2   |     |

#### References and Further Reading

1. Douglas C. Montgomery, "Design and Analysis of Experiments", 5th Ed., John Wiley & Sons, Inc., 2001.

2. Douglas C. Montgomery, George C. Runger, and Norma F. Hubele, "Engineering Statistics", 2nd Ed., John Wiley & Sons, Inc., 2001.

3. Mark J. Anderson and Patrick J. Whitcomb, "DOE Simplified", Productivity Inc., 2000.

4. Ranjit Roy, "A Primer on the Taguchi Method", Van Nostrand Reinhold, 1990.
