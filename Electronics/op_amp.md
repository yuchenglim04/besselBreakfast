The best way to learn op amps is to start from simple ideal models and slowly add more and more complications.

Unity gain buffer:
- simple bare-bones model
- (TI Blogs) Resistors in the feedback of a buffer: Ask why!
- (ADI) Don’t Use the Resistor I Told You to Use
- [What is the purpose of a resistor in the feedback path of a unity gain buffer?](https://electronics.stackexchange.com/questions/56727/what-is-the-purpose-of-a-resistor-in-the-feedback-path-of-a-unity-gain-buffer)
- [How to lower input resistance of buffer (unity-gain) op-amp?](https://electronics.stackexchange.com/questions/643418/how-to-lower-input-resistance-of-buffer-unity-gain-op-amp)
- [Opamp voltage follower with weak positive feedback](https://electronics.stackexchange.com/questions/608127/opamp-voltage-follower-with-weak-positive-feedback?noredirect=1&lq=1)

Non-inverting amplifier:
- Resistor sizing:
  - resistors cannot be too small -> large current exceeding max current output of Op Amp
  - resistors cannot be too large -> greater noise 

Inverting amplifier:
- ideal model
- [Choosing resistor values for inverting amplifier and why?](https://electronics.stackexchange.com/questions/102508/choosing-resistor-values-for-inverting-amplifier-and-why)
- [How do you determine the input impedance for an inverting amplifier?](https://electronics.stackexchange.com/questions/45716/how-do-you-determine-the-input-impedance-for-an-inverting-amplifier)
- [Resistor Load Effect on inverting op-amp](https://electronics.stackexchange.com/questions/229395/resistor-load-effect-on-inverting-op-amp)
- (TI Analog Engineer's Circuit) Transimpedance amplifier with T-network circuit
- (TI Analog Engineer's Circuit) Inverting Amplifier With T-Network Feedback Circuit

Misc:
- [Considerations in resistor sizing for op-amp circuits?](https://electronics.stackexchange.com/questions/599506/considerations-in-resistor-sizing-for-op-amp-circuits)


Bias current:  
- (TI App Report) Importance of Input Bias Current Return Paths in Instrumentation Amplifier Applications
- (Renesas App Note) Operational Amplifiers: How to Bias Op-Amps Correctly
- (TI Technical Article) What You Need to Know about Input Bias Current - and Why

Input, output impedance:
- (Rohm Semicon App Note) Measurement Method for Input and Output Impedance of Op- Amp



Level shifting:  
- (Maxim APPLICATION NOTE 4414) Level Shifting Digital Signals
- [Analog Level Shifting or Level Translating](https://neatcircuits.com/l-shift.htm)
- [ADS1015: Analog Signal level shifting](https://e2e.ti.com/support/data-converters-group/data-converters/f/data-converters-forum/1237978/ads1015-analog-signal-level-shifting)



