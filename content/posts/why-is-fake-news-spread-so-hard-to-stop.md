+++
author = "Alexandros"
categories = ["Machine Learning"]
date = 2021-05-12T21:00:00Z
description = "The hardships in FN detection"
featuredImage = "/images/vxaimuibyt.jpg"
featuredImagePreview = ""
hiddenFromHomePage = false
hiddenFromSearch = false
lightgallery = false
tags = ["fake-news", "machine-learning"]
title = "Why is Fake News Spread so Hard to Stop?"

+++
## Some History

Disinformation is not a recent issue. As Guardian columnist Natalie Nougayr`ede has observed: ”The use of propaganda is ancient, but never before has there been the technology to so effectively disseminate it” [1].

Misinformation, disinformation, and propaganda have been features of human communication since at least the Roman times [2]. However, the invention of the Gutenberg printing press in 1493 dramatically amplified the dissemination of disinformation and misinformation, and it ultimately delivered the first large-scale news hoax - ’The Great Moon Hoax’ of 1835.

![Great-Moon-Hoax-1835-New-York-Sun-lithograph-298px](https://cdn.hashnode.com/res/hashnode/image/upload/v1624355037884/hgEoQsEaU.jpeg) 

As early as 1925, when news offices started to connect via wire, the authenticity of information became a concern. Editors did not know whether the news coming in through the wire was true or not. They could try to infer authenticity based on the source of the news, but still, the concern remained: is this piece of news that just came over the wire true or not?

Although the concern was there, the editors usually managed to find ways to mitigate it and reduce the intentional misinformation to the minimum possible: after all, the amount of news that came over the wire and could potentially be misinformation was not that large.

Unfortunately, the ”tsunami” of social media engagement that has swept our lives over the past decade practically exploded the proliferation of misinformation including the associated distribution of fake news [3].

## Fake News Ecosystems

Someone may consider fake news as false information. Yet, this viewpoint may not be precise.
Instead, researchers usually define it as deliberately false information.

The motivation behind the creation and spread of fake news content may vary. Trend Micro curently sees three major motivations behind fake news [4]: political, financial gain, and character assassination. More analytically, political propaganda is designed to get people to change their minds about their political beliefs or some other opinion. The most obvious financial motivation could be advertising, while character assassination by fake news could target politicians or even private individuals to cause harm.

We now know from related studies, that false information spreads faster than real information [5]. These studies point to the human predisposition in being attracted by novelty - it is known that false news carries more novelty - to explain this. It is not bots that usually spread the misinformation; This is mainly done by humans. Yet the technological processes - social media, algorithmic news curation, bots, artificial intelligence, and big data analysis - are creating echo chambers that reinforce our biases, remove incidia of trustworthiness, and are overwhelming our capacity to make sense the world.

The biggest threat of misinformation is the one that poses to our democracy. Echo chambers ringing with false news can make democracies ungovernable. We can imagine a pluralist democracy in which populations contested elections, without ever sharing a viewpoint on what is going on in the world. Whoever won would design policies to counter what they saw as the major policy question of our times. Since these viewpoints would be isolated and different, such pluralist democracy would be deeply unstable [6].

## The Big Data Problem

Although linguistic methods for fake news detection have achieved a reasonable accuracy, I believe we have reached a barrier.
And that this barrier, that creates a hardship in achieving a better accuracy, is related to the quality of data.

The goal of the style-based (linguistic) methods is to capture the “deception style”, meaning the writing style of fake news writers. Yet, there are some pitfalls with these methods. They may end up capturing the writing style of specific authors instead of the deception style. This way, even if a trained model performs well in similar data, they do not generalize. The writing style of a document is defined by the author, the topic and the editor (if there is one). So, a dataset should contain many authors, news domains and topics.

Finally, as stated in [7], Fake News is a big data problem. We need many data points, solid ground truth and balance over 4 axes: labels, topics, authors and news websites. For example, some datasets are created by downloading articles from websites in a flag-list. However, a website that is found to publish fake news, in order to maintain some credibility, it may also publish credible stories. Creating a dataset this way will add noise to the data and reduce accuracy.

To sum up, to avoid this pitfall, a quality Fake News dataset should have the following properties:

- The ground truth should be solid.
- It should cover many topics.
- It should include different authors and domains that publish articles.

I propose the creation of a fake news data evaluation framework. That framework can perform topic modeling and stylometric analysis to detect unbalanced datasets. A dataset with many data points that also gets a large score at this
evaluation will better generalize in real-world (unseen) data.

## A more Pragmatic Approach

There is a reason why Fake News is so easy to spread. Because it is so close to the “Real” News. Because news (as Fake News does) usually tries to exploit the sentiment of the reader. Provide her with enough negativity and lack of perspective, so that she will be in a constant loop of receiving updates, and give purpose to the papers. The burning issue is not fake news. It’s the news itself.

Fake news is usually a symptom of a deeper pathogen. It’s true that fake news is causing confusion. However, people who are confused end up embracing the fake news.

And this confusion is caused by the lack of transparency, by political inconsistencies, by the lies that are spread and the anger rising on the people’s heart.

Instead of using Artificial Intelligence just to find the “fake stories”, let’s use these tools to understand the underlying societal issues and the malfunctions of the news ecosystem.

## References

1. Natalie Nougayr’ede. In this age of propaganda, we must defend ourselves. here’s how — Natalie nougayr’ede, Jan 2018.
2. A short guide to the history of ’fake news’ and disinformation, Jul 2018.
3. Miriam Fernandez and Harith Alani. Online misinformation: Challenges and future directions.
4. Fake news and cyber propaganda: The use and abuse of social media.
5. Soroush Vosoughi, Deb Roy, and Sinan Aral. The spread of true and false news online. Science, 359(6380):1146–1151, 2018.
6. Yochai Benkler, Robert Faris, and Hal Roberts. Network propaganda: Manipulation, disinformation, and radicalization in American politics. Oxford University Press, 2018
7. Fatemeh Torabi Asr and Maite Taboada. Big data and quality data for fake news and misinformation detection. Big Data & Society, 6(1):2053951719843310, 2019.