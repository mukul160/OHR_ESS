#### Timer Frequency and Period Formula

The timer event frequency is given by:

$$
\text{Timer Event Frequency} = \frac{\text{TIM\_CLK}}{(\text{PSC} + 1) \times (\text{ARR} + 1)}
$$

Where:
- **TIM_CLK** = Timer clock frequency (Hz)
- **PSC** = Prescaler value
- **ARR** = Auto-reload register (counter period) value

To achieve a desired timer period \(T\) (in seconds):

$$
T = \frac{(\text{PSC} + 1) \times (\text{ARR} + 1)}{\text{TIM\_CLK}}
$$

Rearranged for calculation:

$$
(\text{PSC} + 1) \times (\text{ARR} + 1) = T \times \text{TIM\_CLK}
$$
In the example I've written, I've chosen PSC -> 7199 & ARR -> 999
TIM_CLK is 72MHz (from BluePill's clock configuration)
Plugging these numbers into the expression, you'll get a timer event frequency of 10 Hz.

[Back to Part 5](P5_Embedded%20Engineering%20In%20Practice.md)

---