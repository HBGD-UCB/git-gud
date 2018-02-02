# Good `git` for the UCB-HBGD team

The purpose of this document is to provide support for the use of version
control (a lá [`git`](https://git-scm.com/)) in our data analysis and software
development efforts. In order to effectively use the `git` repository available
to us via the HBGDki collaboration, we will reserve that repository for
(cleaned/curated) data sets that will be used in our analysis and demonstration
code. Rather than using the GHAP `git` server to version code we produce, we
will generate and use repos under the HBGD-UCB GitHub Organization. Since we
expect all analysis code to rely on the data sets stored in the private GHAP
`git` repo, there is no need for our analysis code to be held in private
repositories (it ought to be useless to those unaffiliated with our work).

The HBGDki `git` repo is available for cloning (when on a
[GHAP](https://oauth.ghap.io/login/auth#/my-account) session) via

```bash
# ssh user.name@IP
# enter password
git clone https://user.name@git.ghap.io/stash/scm/hbgd-teams/UCB-SuperLearner.git
```

_N.B., the GHAP data repo may only be cloned when logged in to a session
associated with the GHAP system._

Any given `git` repo associated with the software development and data analysis
efforts may easily be cloned from the HBGD-UCB organization. For example, to
clone this repository, try:

```bash
git clone git@github.com:HBGD-UCB/good-git.git
```

Unlike the repo on the GHAP `git` server, all repos affiliated with our GitHub
organization ought to be clone-able from any system (provided your GitHub
credentials are set up properly) -- this means they ought to be accessible when
logged in to a GHAP session or on your local machine.

---

## "Good Enough" Practices

* When developing code (for data analysis or the software products), work on a
    new branch that is aptly named with respect to the functionality you hope to
    add with your work. Commit often, and once you've completed your work,
    generate a [pull
    request](https://help.github.com/articles/about-pull-requests/) to the
    `master` or `develop` branch of the target repo as appropriate.
* We will be using the ["`git` flow" branching
    model](http://nvie.com/posts/a-successful-git-branching-model/). This will
    help keep us on the same page about how and when to create branches as well
    as how to merge new additions to existing long-lasting
    branches (e.g., `develop`).

---

## BAD Practices

The most common bad practice in using `git` is to store your version controlled
repos in a system that provides automatic backups (e.g., Dropbox). DON'T DO
THIS -- especially for repos on which you expect collaborators to contribute.
_Why?_ Well, `git` works by storing snapshots (of the changes in a given
plain-text file between commits) while Dropbox makes near-constant backups. This
has the potential to lead to a conflicting `HEAD`, a problem that no one wants
to resolve.

_tl;dr -- please, please don't use Dropbox with the `git` repos._

---

## Resources

Here are a few useful notes and readings that may be useful in remedying any
problems that may arise when working with `git`. These range the spectrum from
applied to fairly technical:

* ["Version Control with `git`" (Software
    Carpentry)](https://swcarpentry.github.io/git-novice/) - a comprehensive
    introduction to the uses of `git` and social coding with GitHub. This is
    aimed towards students and research professionals.
* ["Happy `git` and GitHub for the useR" (Jenny Bryan,
    RStudio)](http://happygitwithr.com/) - a comprehensive introduction to both
    the inner workings of `git` and best practices in using GitHub, with a focus
    on integrating these tools into your R workflow -- aimed towards
    masters-level university students.
* ["Tools for Reproducible Research" (Karl
    Broman)](http://kbroman.org/Tools4RR/) - a University-level course on best
    practices in modern reproducible research, which includes a couple of
    lectures on `git` and GitHub.
    * ["Version Control with `git` and
        GitHub"](http://kbroman.org/Tools4RR/assets/lectures/04_git.pdf)
* ["Introduction to `git`" (Berkeley's Stat 159/259, Fall 2015, KJ
    Millman)](http://www.jarrodmillman.com/rcsds/standard/git-intro.html) - a
    thorough walkthrough of some common `git` commands as well as explanations
    of what these commands do when invoked.
* ["Elementary `git` with GitHub" (Nima
    Hejazi)](http://nimahejazi.org/posts/git-intro/) - some digest-style notes
    made after reading far more thorough introductions to `git`. These are often
    useful to me when I need to look up a specific bit of core functionality.

