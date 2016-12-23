# Problem description

Santa has 1000 bags to fill to fill with 9 types of gifts. Due to regulations at the North Pole workshop, no bag can contain more than 50 pounds of gifts. If a bag is overweight, it is confiscated by regulators from the North Pole Department of Labor without warning! Even Santa has to worry about throwing out his bad back.

Each present has a fixed weight, but the individual weights are unknown. The weights for each present type are not identical because the elves make them in many types and sizes.

Although the weights were deleted from the database, the elves still have the blueprints for each toy. After some complex volume integrals, the elves managed to give Santa a probability distribution for the weight of each type of toy. To simulate a single gift's weight in pounds, they came up with the following numpy distribution parameters:

```
horse = max(0, np.random.normal(5,2,1)[0])

ball = max(0, 1 + np.random.normal(1,0.3,1)[0])

bike = max(0, np.random.normal(20,10,1)[0])

train = max(0, np.random.normal(10,5,1)[0])

coal = 47 * np.random.beta(0.5,0.5,1)[0]

book = np.random.chisquare(2,1)[0]

doll = np.random.gamma(5,1,1)[0]

block = np.random.triangular(5,10,20,1)[0]

gloves = 3.0 + np.random.rand(1)[0] if np.random.rand(1) < 0.3 else np.random.rand(1)[0]
```
