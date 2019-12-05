# Mobile App for Lottery Addiction

### Project Intro
In this project, we are working with the engineering team of a medical instute who is developing a mobile app to help lottery addicts determine their probability of winning the [6/49 lotto](https://en.wikipedia.org/wiki/Lotto_6/49). Our job is to create the logic and code that will calculate the probability of the user winning given different cases.

### Assumptions:
- For the purpose of this project, we only consider the cases where the user wins by matching 2-6 numbers from the 6 numbers drawn, and ignore any outcomes that involve the bonus number.

### Data:
- [649.csv](https://www.kaggle.com/datascienceai/lottery-dataset): all winning number combinations drawn since the launch of the 6/49 lotto in 1982 up to 2018.

### Project Steps

Since most of our code will rely on probability formulas, the first of the project is setting up two core functions that will be used throughoutthe rest of the project. These functions will each caculate [factorials](https://en.wikipedia.org/wiki/Factorial) and total number of [combinations](https://en.wikipedia.org/wiki/Combination).

Once our core functions are set, we move on to writing the logic to calculate the probability of winning the lottery under different circumstances. Each scenario constitutes a different feature of the app and are as follow:
- probability of winning by playing a single ticket (user inputs their six-number combination)
- probability of winning by playing multiple tickets (user inputs the number of tickets or combinations they're playing)
- probability of getting 2-5 numbers matching from the drawn combination (user inputs number of matching numbers expected)

The institute also requests a feature where users can check their combination against previous drawings and are told how many times their combination has been drawn in the past. For this feature, our function will make use of the historical lotto data in 649.csv, and compare the users combinations against the combinations in the data set.
