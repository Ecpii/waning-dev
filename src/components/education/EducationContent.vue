<script setup>
import TextBlock from '../TextBlock.vue';

</script>

<template>
  <article>
    <TextBlock>
      <b>University of Michigan</b> <br />
      BSE in Computer Science, GPA: 4.000/4.000 <br />

      Coursework:
      <TextBlock>
        <b>EECS 470 - Computer Organization</b> <br />
        <ul>
          <li>
            covers: out-of-order processing (scoreboarding, Tomasulo's, P6, R10K), cache and LSQ design, multiprocessing
          </li>
          <li>
            notes: hard; lot of work. don't recommend taking this accelerated version but also don't regret it.
            content is very interesting and makes a lot of sense but writing this much SystemVerilog drives a man
            crazy.
          </li>
        </ul>
      </TextBlock>
      <TextBlock>
        <b>EECS 482 - Operating Systems</b>
        <ul>
          <li>
            covers: threads, synchronization, virtual memory management, socket programming, filesystems
          </li>
          <li>
            notes: loved this class, though it took a lot out of me! hardest i’ve had to work on a class for but worth,
            structured very well and great staff. content was super interesting and applicable as well.
          </li>
        </ul>
      </TextBlock>
      <TextBlock>
        <b>EECS 483 - Compiler Construction</b> <br />
        <ul>
          <li>
            covers: AST, SSA, x86, Rust, Possible Values Analysis, Register Allocation, lexing and parsing
          </li>
          <li>
            notes: wish i could have focused more on this class - got very overshadowed by 470. projects were
            structured really well and building off instructor solutions was relatively easy! a lot of the
            problems discussed seemed to boil down to "is it undecidable or inefficient? well can we restrict
            the language to get an optimal solution for our smaller search space?". not necessarily a bad thing,
            just kind of an interesting trend.

            <br />

            completely tuned out of most of the lexing, parsing, and grammar lectures but i like how pedagogically
            they were introduced as compiler problems solved by making compilers. the fact that lexer generators
            <b>also</b> have a source language, intermediate language, and semantics ties the course together well
            and cements a prominent key concept overarching the whole class.
          </li>
        </ul>
      </TextBlock>
      <TextBlock>
        <a href="https://www.eecs.umich.edu/courses/eecs497/" target="_blank"><b>EECS 479 - Quantum
            Computing</b></a>
        <ul>
          <li>
            covers: quantum physics fundamentals, Deutsch-Jozaa Algorithm, Grover's Algorithm, Shor's Algorithm, Shor's
            Code, Steane's Code, fault tolerance
          </li>
          <li>
            notes: great class taught by a great professor. took it as a special topics class, content was nonetheless
            very solid and interesting - definitely recommend!
          </li>
        </ul>
      </TextBlock>
      <TextBlock>
        <a href="https://eecs388.org" target="_blank"><b>EECS 388 - Intro to Computer Security</b></a>
        <ul>
          <li>
            covers: cryptography (RSA, Diffie-Hellman, Merkle-Damgård), web security (SQLi, cookies, XSS, CSRF),
            networking (ARP spoofing, DNS attacks), application security (buffer overflows, ROP gadgets, binary
            exploitation), and a lot more
          </li>
          <li>
            notes: did not expect this class to be as useful as it was. It covers a lot more than just security, and I
            can
            not understate how much I have learned about how computers work from this class. It also forced me to get my
            hands dirty with actually looking into binaries using Ghidra and reading out of the x86 manual

            always the ULCS class I recommend to take first because of its breadth
          </li>
        </ul>
      </TextBlock>
      <TextBlock>
        <a href="https://eecs485.org/" target="_blank"><b>EECS 485 - Web Systems</b></a>
        <ul>
          <li>
            covers: React, Jinja, Flask, distributed systems (MapReduce, Google File System), search engines
          </li>
          <li>
            notes: latter half containing non-web dev stuff was interesting to learn about and piqued my interest in how
            distributed systems work. Also interesting exposition to how PageRank works and its parallels to AI.
          </li>
        </ul>
      </TextBlock>
      <TextBlock>
        <a href="https://eecs370.github.io/" target="_blank"><b>EECS 370 - Intro to Computer Organization</b></a>
        <ul>
          <li>
            covers: ARM assembly, single-cycle/multi-cycle/pipeline processor design, low-level code optimization
          </li>
          <li>
            notes: well structured class with a custom ISA that really helped me understand why things are fast/slow on
            computers, and what computers actually can do once we have just a few bits of logic (AND, OR, NOT)
          </li>
        </ul>
      </TextBlock>
    </TextBlock>
  </article>
</template>

<style scoped>
a {
  color: var(--text)
}
</style>
