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
  - "Joanna" - compatibility checking, comformance view
  - "Matt" you're a middle-aged man can't let go of his childhood. show jsbeeb/beebasm

Other features not to forget:
- other languages
- libraries
- shiny new env var/overrides
- tooling
- libraries
- statistics


Fun stufF:
- BBC Micro