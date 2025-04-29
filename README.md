# csed342---assignment-2-sentiment-analysis-solved
**TO GET THIS SOLUTION VISIT:** [CSED342 – Assignment 2. Sentiment Analysis Solved](https://www.ankitcodinghub.com/product/csed342-assignment-2-sentiment-analysis-solved/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;115855&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;CSED342 - Assignment 2. Sentiment Analysis Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
Hwanjo Yu

CSED342 – Artificial Intelligence

General Instructions

This (and every) assignment has a written part and a programming part.

You should write both types of answers in submission.py between

# BEGIN_YOUR_ANSWER and

# END_YOUR_ANSWER

ÒThis icon means a written answer is expected. Some of these problems are multiple choice questions that impose negative scores if the answers are incorrect. So, don’t write answers unless you are confident.

¥This icon means you should write code. you can add other helper functions outside the answer block if you want. Do not make changes to files other than submission.py.

Your code will be evaluated on two types of test cases, basic and hidden, which you can see in grader.py. Basic tests, which are fully provided to you, do not stress your code with large inputs or tricky corner cases. Hidden tests are more complex and do stress your code. The inputs of hidden tests are provided in grader.py, but the correct outputs are not. To run all the tests, type

python grader.py

This will tell you only whether you passed the basic tests. On the hidden tests, the script will alert you if your code takes too long or crashes, but does not say whether you got the correct output. You can also run a single test (e.g., 3a-0-basic) by typing

python grader.py 3a-0-basic

We strongly encourage you to read and understand the test cases, create your own test cases, and not just blindly run grader.py.

Advice for this homework:

• Words are simply strings separated by whitespace. Don’t normalize the capitalization of words (treat great and Great as different words).

• You might find some useful functions in util.py. Have a look around in there before you start coding.

Problems

Problem 1. Hinge Loss

Here are two reviews of “Frozen,” courtesy of Rotten Tomatoes (no spoilers!):

Rotten Tomatoes has classified these reviews as “positive” and “negative,” respectively, as indicated by the in-tact tomato on the left and the splattered tomato on the right. In this assignment, you will create a simple text classification system that can perform this task automatically.

Problem 1a [2 points] Ò

We’ll warm up with the following set of four mini-reviews, each labeled positive (+1) or negative (−1):

• (+1) pretty good

• (−1) bad plot

• (−1) not good

• (+1) pretty scenery

Each review x is mapped onto a feature vector φ(x), which maps each word to the number of occurrences of that word in the review. For example, the first review maps to the (sparse) feature vector φ(x) = {pretty : 1,good : 1}. Recall the definition of the hinge loss:

Losshinge(x,y,w) = max{0,1 − w · φ(x)y},

where y is the correct label.

Suppose we run stochastic gradient descent, updating the weights according to

w ← w − η∇wLosshinge(x,y,w),

once for each of the four examples in order. After the classifier is trained on the given four data points, what are the weights of the six words (‘pretty’, ‘good’, ‘bad’, ‘plot’, ‘not’,

‘scenery’) that appear in the above reviews? Use η = 1 as the step size and initialize w = [0,…,0]. Assume that ∇wLosshinge(x,y,w) = 0 when the margin is exactly 1.

Problem 2: Sentiment Classification

In this problem, we will build a binary linear classifier that reads movie reviews and guesses whether they are “positive” or “negative.”

Problem 2a [2 points] ¥

Implement the function extractWordFeatures, which takes a review (string) as input and returns a feature vector φ(x) (you should represent the vector φ(x) as a dict in Python).

Problem 2b [8 points] ¥

We’re going to train a linear predictor, which can be represented by a logistic regression model. Here is the definition of linear predict:

if w · φ(x) &gt; 0 if w · φ(x) &lt; 0

where σ is a logistic(or sigmoid) function.

Your task is to implement the function learnPredictor using stochastic gradient descent, minimizing the negative log-likelihood loss (NLL) defined as:

LossNLL(x,y,w) = − log(pw(y | x))

You should first derive ∇wLossNLL(x,y,w), then exploit the formula to update weights for each example. Also, you can print the training error and test error after each iteration through the data, so it’s easy to see if your code is working.

Problem 2c [3 points] ¥

The previous features include unigram(single) words only, which cannot consider the context of a word in an utterance. In this task, we’ll incorporate bigram words into features. In other words, features include pairs of consecutive words. Implement extractBigramFeatures which extract both unigram and bigram word features.

Problem 3: K-means Clustering

Problem 3a [2 points] Ò

Suppose we have a feature extractor φ that produces 2-dimensional feature vectors, and a toy dataset Dtrain = {x1,x2,x3,x4} with

1. φ(x1) = [0,0]

2. φ(x2) = [0,1]

3. φ(x3) = [2,0]

4. φ(x4) = [2,2]

Run 2-means on this dataset. What are the final cluster centers µ? Run this algorithm until it converges, with initial centers:

1. µ1 = [1,−1] and µ2 = [1,2]

2. µ1 = [−2,0] and µ2 = [3,−1]

Problem 3b [6 points] ¥

Implement the kmeans function. You should initialize your k cluster centers to random elements of examples.

After a few iterations of k-means, your centers will be very dense vectors. In order for your code to run efficiently and to obtain full credit, you will need to precompute certain quantities. As a reference, our code runs in under a second on all test cases. You might find generateClusteringExamples in util.py useful for testing your code.
