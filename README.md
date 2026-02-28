# HV-PS-design

I used ChatGPT 5.0 to work through the design of a boost supply for 15V to
~200V at 2-4W. Initially I used a target inductor size of 100mH when I meant 100uH! It picked up the difference and suggested that for continuous operation (CCM) 8-15mH would be better. The 'basic-ps-design.md' file has that 'revelation' along with a handy formula for picking the inductor size based on a ripple current level:

Solve $L=\dfrac{V_\text{in}D}{\Delta I\,f_\text{sw}}$ using $\Delta I = \rho\, I_\text{in}$.

Where the ripple current is $ \rho $: 20% ripple $ \rightarrow \rho = 0.2 $

And $ I_\text{in}$, the Input (inductor average) current, is

$I_\text{in} \approx \dfrac{P_\text{out}}{\eta\,V_\text{in}} \approx \dfrac{2}{0.85\cdot 15} \approx 0.157\text{ A}$.

Where $\eta$ the PS efficiency is 85%


