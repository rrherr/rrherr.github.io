## Picasso's Bulls: Deconstructing his design process with Python

### Description
In 1945, Picasso created a [series of 11 bulls](https://www.nortonsimon.org/art/search-the-collection/result?keyword=picasso+bull&earliest_year=1945&latest_year=1946). He started by drawing a realistic bull, and then he made it more and more abstract. The bulls fascinate people because we can see his process and follow along step by step.

Picasso said, "A picture used to be a sum of additions. In my case a picture is a sum of destructions. It would be very interesting to preserve the metamorphoses of a picture. Possibly one might then discover the path followed by the brain in materializing a dream."

We can explore this, with Python! Using Picasso's "version control history", we'll create "git diffs" to show changes between bulls, with additions in green and "destructions" in red. We'll use Jupyter Notebook to show our work, like Picasso.

The tools we create will help us see what choices Picasso made, and why he made them. It wasn't arbitrary. He was designing and solving puzzles!

Picasso found the right abstractions to simplify his work. We aspire to do this, too! Making software can help us understand Picasso, and understanding his process can help us make software. 

### Audience
(1) Who is this talk for?

This talk is for people with interdisciplinary interests in art and code, who are looking for creative inspiration more than practical application. I believe when people read the talk's title and description, some will say, "Ooh, sounds fascinating!" and others will say "Hmm, sounds weird." That's good, because people will be able to decide accurately whether this talk is for them!

(2) What background knowledge or experience do you expect the audience to have?

The talk is accessible for beginners. Anyone who is curious about the topic and has some programming experience will be able to follow along. There is no machine learning involved.

I use libraries like scikit-image and numpy, but I don't expect any prior experience with them. For example, here's the core code to make image diffs, which I explain line by line in detail, with a Jupyter Notebook:

```
# a, b are binary images in numpy arrays
unchanged = a & b
deleted = a & ~b
added = ~a & b
```

```
# img is a color image in a numpy array
img[deleted] = red
img[added] = green
img[unchanged] = black
```

(3) What do you expect the audience to learn or do after watching the talk?

I hope the audience will be inspired to think differently and creatively about their software design process! 

### Outline
- What does Picasso's process have to do with Python programming? (2 minutes)
- Do you ever feel stuck, when you're making something? Even Picasso got stuck sometimes (2 minutes)
- Picasso got unstuck with a new process, and created his series of 11 bulls (4 minutes)
- To understand the process, let's look at image diffs (4 minutes)
- Here's how to code the image diffs in a Jupyter Notebook (4 minutes)
- Let's look at an animation, and walk through it line by line, to see how Picasso was solving puzzles! (6 minutes)
- Let's look at another representation (such as silhouettes or line simplification algorithms) and code in a Jupyter Notebook (5 minutes)
- Conclusion (1 minute) 

### Additional notes
I presented a version of this Picasso talk at Strange Loop in September 2018.
- Video: https://www.youtube.com/watch?v=GYJ77F_8kq0
- Image diffs, examples: https://twitter.com/rrherr/status/1039910057784303617
- Image diffs, Jupyter Notebook: https://gist.github.com/rrherr/011108f76daaede5b1e9076bf2d03da1
- Animation between states: https://twitter.com/rrherr/status/1045290499123408896

I'm refining the talk for PyCon and excited for the opportunity! If my talk is selected, I may need to be scheduled on the first day of the conference.

I have additional speaking experience, doing "show & tell" with Python code in Jupyter Notebooks:
- I presented a talk at Deconstruct in May 2018, called "Let's Program a Banjo Grammar." https://www.deconstructconf.com/2018/ryan-herr-lets-program-a-banjo-grammar
- I'm a data science instructor at Lambda School, where I teach live online classes. 
