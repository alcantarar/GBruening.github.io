---
layout: single
classes: wide
title: "Literature Update"
excerpt: "Using machine learning to predeict biomechanics paper topics."
header:
collection: project
permalink: /projects/lit_update
author_profile: true
share: true
---

Biomechanists have been searching for papers, classifying them, and sharing this classification with the community for many years to assist in disseminating recent research. These have been posted on the [Biomech-L](https://biomch-l.isbweb.org/forums/7-Literature-Update) website in their forum posts as a weekly update. This process however takes a lot of work, and we are very grateful to every person who has posted these here, but we thought thats a little to much work.

So [Ryan Alcantara](https://alcantarar.github.io/) and I developed a system that uses machine learning to be able to find these papers and predict the topic with a few clicks. We wrote a webscraper that crawled the forum posts from the past 10 years and pulled 53,652 papers. We then sorted those papers, pulled abstracts, and parsed the papers into a format for the machine learning.

We then applied multiple [supervised machine learning](https://towardsdatascience.com/supervised-machine-learning-classification-5e685fe18a6d) techniques to the data set. A deep neural network implemented using TensorFlow and Keras proved the have the best predictive accuracy of about 73.5%. Many papers could have multiple possible classifications, and by an eye check the method seems to be doing pretty well. 

Once the model was created, we created a python notebook that uses the [BioPython](https://biopython.org/) search engine to search PubMed for recent papers that have Biomech or Locomot in the the title or abstract. The data is then fed into the model to predict the topic, sort them by topic, and then create a markdown file to publish online. Two early literature updates can be found [here](https://gbruening.github.io/litupdate/), but in the future I won't post new ones and just link to [Ryan's Literature Updates](https://alcantarar.github.io/literature/).

If you'd like to see the code that did all this, you can find it [here](https://github.com/alcantarar/literature_update).

<figure class ="align-center">
    <a href="/images/biomchL_predict_plot_DNN.png"><img src="/images/biomchL_predict_plot_DNN.png"></a>
    <figcaption>Percent of correct predicted topics on a sample test set of the full dataset. 5% of the papers were used for validation.</figcaption>
</figure>
