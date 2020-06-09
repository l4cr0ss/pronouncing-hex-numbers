# pronouncing-hex-numbers
How to pronounce hex numbers and not trip over your own tongue

#### Motivation
  1: reading hex phonetically is annoying  
  2: repeating yourself because you failed to make yourself understood sucks
  3: existing proposals for pronouncing hex are over-engineered, unrealistic, and/or vulgar sounding.

#### Goal 
  1: consistent set of rules for dictating hex numbers  
  2: easy to remember, easy to say, easy to understand  
  3: no "special" additional knowledge  
  4: (IMPORTANT) as not-ridiculous-sounding as possible  

#### Rules
```
  1: read the number from left to right, two bytes at a time ("blockwise")
  2: while blocks remain, consume a block and...:
       if only the leading nibble is set:
         call out the block using traditional english comma notation
         (ex: `0x8000` → "ate-thousand", `0xE000` → "e-thousand", etc.)
       else if all nibbles are the same:
         call out "X block", where X is the repeated nibble
         (ex: 0xFFFF → "f-block", 0x2222 ← "two-block", etc.)
       else:
         call out both bytes in the block of nibbles
         (ex: 0xCAFE → "c'ity-alfa", "ef'ity-ecko")
         OR
         (ex: 0xCAFE → "charlie-alfa", "foxtrot-ecko")
         OR
         (ex: 0xDE45 → "delta-ecko", "fourty-five"
```

#### Example
  By using this simple set of rules you can dictate hex numbers of arbitrary complexity 
    ex: `0x7FFF FFFF FFFF 7000 4534 FE23 D000 87EE C9FE 9090 323A BDFF`

```
        0x7FFF → "seventy-ef, foxity-ef"
        0xFFFF → "f-block" 
        0xFFFF → "f-block" 
        0x7000 → "seven-thousand" 
        0x4534 → "fourty-five, thirty-four"
        0xFE23 → "foxity-ecko, twenty-three"
        0xD000 → "dee-thousand"
        0x87EE → "eighty-seven, eckity-ecko"
        0xC9FE → "charlotty-nine, efity-ecko",
        0x9090 → "ninety, ninety" (OR "nine-thousand-ninety"),
        0x323A → "thirty-two, thirty-alfa",
        0xBDFF → "bravity-delta, efity-ef"
```

#### _Example_ pronunciation guide
  It *doesn't matter* if you use these pronounciations. 
  What matters is you 1) *stick to four nibbles*, and 2) *remain intelligible*.

```
      0: zed       0x: zero-'x' or zed-'x' or '0day', etc.
      1: one       1x: eleven'ty-'x'
      2: two       2x: twen'ty-'x'
      3: three     3x: thir'ty-'x'
      4: four      4x: four'ty-'x'
      5: five      5x: fif'ty-'x'
      6: six       6x: six'ty-'x'
      7: sev(en)   7x: seven'ty-'x'
      8: ate       8x: eigh'ty-'x'
      9: niner     9x: nine'ty-'x'
      A: a         Ax: ace'ity-'x'
      B: b         Bx: b'ity or "brahv'ity" 
      C: c         Cx: c'ity or "charlot'ty" 
      D: d         Dx: d'ity or "deity"
      E: e         Ex: e'ity or "eckity"
      F: f         Fx: f'ity or "foxy" or "foxity"
```
