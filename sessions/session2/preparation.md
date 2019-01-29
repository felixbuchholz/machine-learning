# Week 2 discussion questions

## Weekly case study [link](https://www.wired.com/2015/07/google-says-ai-catches-99-9-percent-gmail-spam/)

### 1. What are the primary goals of spam filters? And how should their success be measured?

The primary goal of these filters is to remove unwanted messages from the email inbox and collect them separately. Success should not only be measured as the rate of unwanted mail detected but also contrasted with the measure how many wanted mails are falsely identified as spam – it is a combined measure. 

### 2. What is a “heuristic” approach, in computing? 

An approach to solve a problem is called heuristic when the ideal or optimal solution to that problem is not known or knowingly not pursued in exchange for a greater resource efficiency.

#### An analysis of trade-offs of an heuristic can be done in the following domains: 

- Optimality: Does the heuristic guarantee the best solution? Is it actually necessary?
- Completeness: Can the heuristic find all the best solutions? Do we actually need all of them?
- Accuracy and precision: Can the heuristic provide a confidence interval for the purported solution? Is the error bar on the solution unreasonably large?
- Execution time:  Is this the best known heuristic for solving this type of problem?

### 3. How do you personally define “spam?” (No Monty Python jokes, please.) 

For me personally spam is any message I don’t want to react on in any way (read something further, respond, take another action)


## Alpaydin Preface and Ch. 1

### 1. What is the significance of the movement from human-coded algorithms to machine-defined algorithms? Is this approach better or worse? Why?

- “For some tasks, we do not write programs but collect data.”
- “The data contains instances of what is to be done, and the learning algorithm modifies a learner program automatically in such a way so as to match the requirements specified in the data.”
- The “dataquake” and increased knowledge in machine learning made this shift in paradigms possible. 
- The reason for and the belief hidden in the use of machine learning is that there is a pattern to the data, even though it is big and complex

“In machine learning, the aim is to construct a program that fits the given data. A learning program is different from an ordinary computer program in that it is a general template with modifiable parameters, and by assigning different values to these parameters the program can do different things. The learning algorithm adjusts the parameters of the template — which we call a model — by optimizing a performance criterion defined on the data.” (p. 23 f)


### 2. What are the cultural shifts and developments in technology over the past century that have led to the ubiquity of machine learning? 

- Instead of thinking that AI could be achieved by a completely new form of algorithm or a new approach to computation it seems like intelligence is best approximated by simple, straightforward algorithms combined and trained with huge amounts of data

- Computers store data
- Then they exchange it
- Everything goes mobile
- Social media

Now we are constant producers of data: 

“With the number of smart machines continuously helping us in our daily lives, we all became producers of data. Every time we buy a product, every time we rent a movie, visit a Web page, write a blog, or post on the social media, even when we just walk or drive around, we are generating data. And that data is valuable for someone who is interested in collecting and analyzing it. The customer is not only always right, but also interesting and worth following.”

### 3. How does your grocery shopping differ on the night before a big blizzard? (Compared to your normal grocery shopping.) How might machines predict your behavior? 

Shopping before a big blizzard is probably influenced by the fear of not being able to go shopping the next days. Machines could predict this behavior by comparing customer data with weather reports.

### 4. How does Alpaydin define “artificial intelligence?” And “machine learning?” What is the role of machine learning in artificial intelligence? 

AI: Artificial Intelligence is a form of computational problem solving where the strategy and solution to a problem is not specifically implemented for every situation, instead the mechanism can adapt to a new situation and solve the problem appropriately. 
ML: Machine learning is a category of artificial intelligence algorithms that find solutions to new problems after they have been trained on large data sets with similar cases of the problem. 

Machine learning is the driving force (most used method) in artificial intelligence right now, but machine learning is only a subset to ai.

- “This is called data mining. The analogy is that a large volume of earth and raw material is extracted from the mine, which when processed leads to a small amount of very precious material. Similarly in data mining, a large volume of data is processed to construct a simple model with valuable use, such as having high predictive accuracy.
Data mining is one type of machine learning. We do not know the rules (of customer behavior), so we cannot write the program, but the machine — that is, the computer — “learns” by extracting such rules from (customer transaction) data.”

### 5. How do computers become more intelligent? 

By using more and more data and by improving the knowledge around learning algorithms.

### 6. In computing, how do we get from bit sequences (such as “101100” or “1000001”) to numbers, words, images, sounds, colors, and interactivity?  

- The binary data stored gets interpreted by a program (an algorithm) that translates the data into the expected output, according to the data format.

### 7. When is a “good and useful approximation” better than a precise and rigorous approximation? Why? 

- “That approximation may not explain everything, but may still be able to account for some part of the data.”

### 8. What are some of the major sources of data? 

- Human: All of our recorded digital behavior, texts and recordings
- Physical: Sensors & machine vision

### 9. What role does our understanding of the human brain have in our attempts to develop artificial intelligence? What are the limitations of trying to mimic (our understanding of) the brain? 

As of today the (some) learning algorithms so called artificial neural networks try to mimic the structure of the brain: layers of neurons connected by synapses where processing and memory is not as clearly separated as in a computer: the connection of the synapses establishes the memory but also is the way the distributed processing units, neurons, are connected.

### 10. What are the limits of learning? 

- In the future we might not mimic the brain as closely anymore but find the underlying laws of learning.

### 11. Practical considerations: 

First, we should keep in mind that just because we have a lot of data, it does not mean that there are underlying rules that can be learned. 

Second, the learning algorithm itself should be efficient, because generally we have a lot of data and we want learning to be as fast as possible, using computation and memory effectively. In many applications, the underlying characteristics of the problem may change in time; in such a case, previously collected data becomes obsolete and the need arises to continuously and efficiently update the trained model with new data.

Third, once a learner has been built and we start using it for prediction, it should be efficient in terms of memory and computation as well. In certain applications, the efficiency of the final model may be as important as its predictive accuracy.

## Flach pp. 1 - 20

### 1. How does Flach define “machine learning?”

“Machine learning is the systematic study of algorithms and systems that improve their knowledge or performance with experience.”

- “(…) machine learning is concerned with using the right features to build the right models that achieve the right tasks.”

### 2. In detail, describe the inner workings of a spam filter.

A spam filter **uses a model of distinctive features** of emails that can contribute to a classification as wanted or unwanted mail. These features can be for example specific words but also combined indicators like the text to image ratio. 
To distinguish between those each feature gets a **score** and if the combined score is above a certain **threshold**, the email gets flagged as “junk”. The score for each feature is called weight and the process of adjusting the weights to get a proper classification of spam is the machine learning process.

There are three different approaches to reach the classification goal and there are learning algorithms optimized for each of them:

- A linear statistical approach to find the equation that describes the separating “line” between the emails features
- A probability based on a Bayesian quotation
- A rule-based example with logical, binary decision trees

### 3. What is “overfitting?” 

If a model is trained in such a way that it is too adjusted to the training data and doesn’t perform as expected on new data. 
- But: The training data also has to be **representative**!

### 4. In Figure 3 on p. 11, Flach presents a framework for the process of machine learning. Describe it and define each of the individual components. 

The figure is a flow diagram that shows the problem solving process from the input to the output stage. The input of a certain domain consists of objects that have features. The domain is the sphere & scope of the problem, for example face recognition of passengers at an airport. The objects in this case are the passengers but they are represented by the images of whatever imaging technology is used for this case. These images have features and are described as data, most probably pixels with lightness, hue and saturation information. The process of converting the data (the images) via a model (that identifies the people) to achieve the desired output is the task, while the process of gaining the right parameters for that model is the learning problem. A model is used by training a learning algorithm to produce the desired weights (parameters for the problem) with a sample of representative data.  

### 5. What are some of the “tasks” that machine learning can solve? 

### 6. Share some examples of when you’d “predict” and when you’d “describe.” 

### 7. How do we evaluate performance on a machine learning task? 

### 8. Practical considerations: 

Machine learning is all about 

1. Using the right features 
2. to build the right models 
3. that achieve the right tasks.


## Matthes Ch. 9

### 1. In Python, what is a “class”?
- 
### 2. What are some good reasons to use classes in programming? 
- 
### 3. What is a “module”? How do you access classes in modules? 
- 
### 4. What is a “method”? And when do you use methods? 
- 
