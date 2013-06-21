l
tex-therefore
===============

Tired of needing to come up with synonyms for 'Therefore,' in your mathematical writing? Ponder no longer! This LaTeX package provides a macro to carefully select one of a multitude of choices.

As an example, please see [sqrt_two.pdf](https://docs.google.com/file/d/0B5P_UFIGCcUaOWxxeEVoNGp4ZlU/edit?usp=sharing).

This project was inspired by the thread at http://www.reddit.com/r/math/comments/1gov71/mathematical_writing_synonyms_for_therefore/ particularly 

```
lucasvb: Someone should collect these into a macro.
    perpetual_motion: We need a command that would just insert one at random.
```

If you have suggestions for more phrases to include or want to write another example proof, feel free to fork/pull the repo. If you're not on GitHub, feel free to email me your additions at bgschiller@gmail.com.

Usage
-----

Download the file therefore.sty to the directory where your LaTeX file is. In the preamble, put

```latex
\usepackage{therefore}
```

Wherever you would otherwise laboriously choose a synonym for 'Therefore', simply type

```latex
\Therefore there are an infinite number of primes
```

Notice that there is no trailing comma after `\Therefore`. This is because some of the transitions, such as 'And verily it goes that', do not require commas. If one is needed, it will be part of the expansion. 

The macro will expand differently with each compile. The choice of seed used each time is documented in `your_file.log`. For example, 

```
many lines of output here
...
Random number generator initialized to 379457
...
more lines of output here
```

 If there is a result you particularly like, you can choose it by passing a `seed=379457` option to the package:

 ```
 \usepackage[seed=379457]{therefore}
 ```
