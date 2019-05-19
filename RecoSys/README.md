# SVN recommendation Sytem

## Environments

1. Anaconda (https://www.anaconda.com/)
2. Install Spyder in Anaconda
3. Install `scikit-surprise` in Anaconda environment if needed (https://anaconda.org/conda-forge/scikit-surprise)

## Run the sample

1. Open Sypder.
2. Open all files in the folder `SVNreco` in Sypder.
3. Run `SVDBakeOff` or `SVDTuning`, it may take a while because it has algorithm evaluation feature (you can see the evaluation result if you set `evaluator.Evaluate(True)`).
4. You can test your own movie recommendations if you add your movie rating in the file `ratings.csv` (user 672 is an example). (more data more accurate).

## Example of out put

```
Building recommendation model...
Computing recommendations...

We recommend:
Gladiator (1992) 4.259103540244643
Dark Knight, The (2008) 4.188242932936566
Wallace & Gromit: A Close Shave (1995) 4.185875068587718
Fight Club (1999) 4.168733743550588
Eat Drink Man Woman (Yin shi nan nu) (1994) 4.1635112964419045

Using recommender  Random

Building recommendation model...
Computing recommendations...

We recommend:
Dumbo (1941) 5
Fly, The (1986) 5
Usual Suspects, The (1995) 5
Crimson Tide (1995) 5
Interview with the Vampire: The Vampire Chronicles (1994) 5
```
