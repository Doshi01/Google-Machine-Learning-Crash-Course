```python
import numpy as np

# Call np.array to create a NumPy array with your own hand-picked values.
two_dimensional_array = np.array([[6, 5], [11, 7], [4, 8]])

# You can populate an array with a sequence of numbers:
# np.arange generates a sequence that includes the lower bound (5) but not the upper bound (12).
sequence_of_integers = np.arange(5, 12)

# The following call populates a 6-element array with random integers between 50 and 100.
random_integers_between_50_and_100 = np.random.randint(low=50, high=101, size=(6))

# To create random floating-point values between 0.0 and 1.0, call np.random.random
random_floats_between_0_and_1 = np.random.random([6])

random_floats_between_2_and_3 = random_floats_between_0_and_1 + 2.0

random_integers_between_150_and_300 = random_integers_between_50_and_100 * 3


```