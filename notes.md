#### Notes

Time budget: 60m
- 5m intro
  - why/when/how/who
- 5m overview / crash course
  - Design Ethos
    - Perfect is the enemy of good enough
    - Need to fit a number of use cases
    - Small-er screens? (mobile, er look puppies)
  - Windows, parent/child aspect
  - Output options vs Filters
  - Extra compiler panes vs Tools
  - Compiler Selector
    - search
    - favourite
    - popout
- 5m continued^^
  - don't go overboard on the tools etc, as it is something for later
- 5m Jordan's Tale
  - An "HFT" dev looking to improve performance
  - std::accumulate vs hand-rolled
  - perf investigation with llvm-mca
```c++
#include <numeric>

int sum(int *array, std::size_t num) {
  __asm volatile("# LLVM-MCA-BEGIN");
  return std::accumulate(array, array + num, 0);
  __asm volatile("# LLVM-MCA-END");
}
```
   - analysis view, diff view
- 5m ''
- 5m Jason's Tale
- 5m ''
- 5m Compiler Developer
- 5m Matt's Tale
- 5m the future/how you can help
  - stats
  - budget?
  - dreams; logins, links, live updates, CPU emulation
  - Support us by ubmitting issues, PRs, or patreon, github. supporting our sponsors
- 5m questions
- 5m contingency

Ideas:
- Quick overview of design and explain?

- tell story in terms of users?
  - "Jordan", a HFT developer wanting to see what overhead using STL algos are compared to "just" writing a loop
      - can show diff view
      - can show tools like OSACA
      - Demo LTO and thus IDE mode
      - Templates
  - "Mason" - C++ YouTuber or educator who wants to quickly demonstrate languages, execute only, libraries. teach folks. show asm popups, CFG window. Sonar, clang-tidy, readelf, env var overrides
  - "Reg" - Compiler Developer, clang-query, llvm AST view
  - "Matt" you're a middle-aged man can't let go of his childhood. show jsbeeb/beebasm

Other features not to forget:
- other languages
- shiny new env var/overrides
- tooling
- libraries
- statistics


Fun stufF:
- BBC Micro


NEED TO SHOW CODE EXECUTION
GPU?

STATS


---- notes

run trhgouh one overran hugely

run through two
- intro took 5m yay
- 15 to do the "ux overview" and had a number of things I missed out, like compiler picker (!)
  - probably too apologetic?
- 10m to get to end of "Jordan"
- 10m to get mostly through "Mason", maybe 5m more
- 10m for "Joanna" but honestly was rushed and not clear. Maybe more direct links by now
- ZOOMED throguh rest and future and no time for questions

--- third runthru at work
* 10m to intro
* 13m to do UX overciew
* 21m to to end of Mason
* 18m to end ... but rushed
  - got a good laugh at "matt"

Suggestions:
- Reg -> cal it CE User Journeys?
- Yijie -> also users "security researcher" looking for stack overlow, injection spots etc
- Suggestion to drop the UX overview entirelys
  - more time
  - it comes out more naturally in the user journeys
- Suggestions from tao
  - why:
    - The concrete example with range for is nice; would suggest starting off with the anecdote although some will have heard it before
  - how:
    - A system diagram to help audience appreciate complexity
    - Touch upon ballpark of costs which provides an organic segue towards thanking sponsors (and incepting the idea of audience members becoming sponsors)
  - timelines
    - Names with the faces; perhaps augmented with number of commits or a big feature they're proud of
    - Alternatively it would be good to include them and some "and the rest of our open source contributors" on the closing card
  - names of archetypes
    - Picture (possibly GPT-generated, kind caricatures)
