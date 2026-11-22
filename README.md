# Memory Lab

A browser lab for Session 17 of *Introduction to Neuroscience* (Krea University):
"Learning, memory and plasticity I: an introduction to the changing brain" (Bear, Connors &
Paradiso, Ch. 24). Three short parts, each opened by a password shown on its lab slide.

1. **Mirror hands** (about 8 min). Trace a five-pointed star while up and down are swapped,
   as in Brenda Milner's mirror-drawing test with Henry Molaison (H.M.). One practice trace in a
   normal view, then five mirrored traces. The lab records time and how often the pen leaves the
   track, and draws a learning curve. Each trace stops after 75 s.
2. **Cells that wire together** (about 8 min). A 12 × 12 Hopfield network (Hopfield, 1982)
   trained with Hebb's rule (w<sub>ij</sub> += x<sub>i</sub>x<sub>j</sub>, cells coded ±1). Students teach
   it three pictures, give it a noisy or partial cue and watch it settle (pattern completion),
   cut connections (graceful degradation, a gentle nod to Lashley), and overload it with random
   memories (interference). The pictures were chosen to be nearly uncorrelated. Updates are
   asynchronous with a fixed random order, and lesions and extra memories use fixed seeds, so
   everyone in the class gets the same numbers. With the defaults, the noisy cup is recalled
   perfectly with 0% and 50% of connections cut, about 92% with 90% cut, and fails (about
   72%, a blend) after 15 random memories are added.
3. **Remembering is rebuilding** (about 6 min). The Deese–Roediger–McDermott task: four lists of
   ten words (the first ten associates of *sleep*, *sweet*, *cold* and *doctor*, after
   Roediger & McDermott, 1995), shown at 1.5 s per word; 30 s of quick sums; then a 24-item
   recognition test (12 studied words, the 4 theme words that were never shown, 6 unrelated new
   words, and 2 theme words of lists that were not shown: *chair*, *window*), with a confidence
   rating. The results page compares "seen" responses for studied words, the never-shown theme
   words, and unrelated words.

**Privacy:** nothing is saved or sent. Students write their numbers on paper.

**Passwords:** `mirror`, `assembly`, `rebuild`. Change `PASSWORDS` near the top of the script
in `index.html`, and `\labpw` in the slides. Letter case and spaces are ignored. This paces the
class; it is not security (anyone who reads the page source can find the words). Once a part is
unlocked it stays open in that browser tab.

**Testing:** add `?fast=1` to the address for short timings (8 s trace limit, 0.12 s words,
3 s pause). Do not use it in class.

**Accessibility:** large type (Atkinson Hyperlegible), no sound, no flashing, dark mode follows
the device. The network animation is instant when the device asks for reduced motion. Works on a
laptop or a phone held sideways; Part 1 needs a mouse, trackpad or finger.

## Publishing on GitHub Pages

1. Create a new **public** repository named exactly `memory-lab` (the slides' QR code expects
   this name).
2. Upload everything in this folder, keeping the `lib/` folder and the hidden `.nojekyll`.
3. **Settings → Pages**: Deploy from a branch, branch **main**, folder **/ (root)**, Save.
4. After a minute or two: `https://rakesh-sengupta.github.io/memory-lab/`

## Credits

Built with jsPsych 7.3.4 (de Leeuw, 2015, *Behavior Research Methods* 47, 1–12; MIT licence,
in `lib/`). Mirror drawing after Milner (1962) and Milner, Corkin & Teuber (1968,
*Neuropsychologia* 6, 215–234). Network after Hebb (1949) and Hopfield (1982, *PNAS* 79,
2554–2558). Word lists after Roediger & McDermott (1995, *JEP: LMC* 21, 803–814).
