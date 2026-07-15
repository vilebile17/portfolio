# Function Finder

[<- Back Home](/)

[<- Back to Projects](/projects)

## Project Rundown

- **Time Span** -> 3+ hours
- **Completed** -> July 2026
- **Git Repository** -> [Github](https://github.com/vilebile17/nonsense/blob/main/function_finder.py)

![some graph](/images/some-graph.png)

![This uses](https://skillicons.dev/icons?i=py)

## function_finder.py 

To be honest, this isn't _really_ a project; I built this little guy in an afternoon after all. I am however
_really_ happy with how it turned out and I _definitely_ enjoyed the building process.

If you couldn't tell already, this python code finds a [polynomial](https://en.wikipedia.org/wiki/Polynomial) that goes through a set of coordinates
that the user inputs. For example, if you run: `python3 function_finder.py '(0,4)' '(10,4)' '(-4,-7.088)' '(7,1.921)'`
you get that random function I put into [desmos](https://desmos.com/calculator) for that image just above: `f(x) = 0.027x^3 - 0.36x^2 + 0.9x + 4.0`

It even works decently well with _non-polynomial_ functions; here's its attempt at `e^x` when given the values of `e^x` for integer values
of x from -2 to 5 inclusive: 

![e^x graph](/images/e^x.png)

This exact same program can be used to find the _nth-term_ of a _polynomial sequence_, just instead of x and y coordinates you input
which term of the sequence it is and what the actual value of that term: `(n, uₙ)`

### How does it work?

Put simply, it goes through each point and tweaks its estimate of the polynomial each time by adding a term with a power one higher than
the last one.

If we had the coordinates: `(1,2)`, `(2,6)`, `(3,12)` it would first make a function that goes through the first point: `f(x) = 1` which is
just simply a horizontal line.

Then it would take into account the second coordinate and build a function that looks like this: `f(x) = 1 + 4(x-1)` notice that it just adds another
term to the end of the function (we've retained the `1` from the beginning) and it keeps it factorised until the end. If we were to try `f(1)` again
then the right term would become zero (4·0 = 0) this means that we get the exact same value that we got before adding the new term!

For the third point it would again add another term, now the function is `f(x) = 1 + 4(x-1) + 1(x-1)(x-2)`. Notice that if we were to substitute either of
the last two x-values (`1` or `2`) then the right most term would become zero; this is why we can keep on adding terms _non-destructively_.

Anyway, we've now exhausted all of our coordinates (and your brain if you were trying to follow along) and so that's the final function.
The program then multiplies out the brackets and collects like terms to get the function `f(x) = x^2 + x`

The method that is used in this algorithm was taught in one the problem-solving workshops held by [ULMaS](https://liverpoolmathsschool.org/index.asp)

### AI usage

This is one of the few projects where I used **absolutely no AI**; no code edits, no problem-solving. **Nothing**. Even with
my [other projects](/projects) AI usage is _minimal_; 90%+ of the code is written by me and basically 100% of problem-solving
