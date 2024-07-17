**Google** has a design doc driven culture. 
- Google has something called one-pager, which tends to go over on-page
- but, typical design doc tends to be pretty long, ranging from 3 to 12 pages
- John Ousterhout's "A Philosophy of Software Design" is a good book on the subject. He has worked with Google.
- The design process at Google started with a design document. There was a template that I think was available online a long time ago but (ironically) I can no longer find it. The template was relatively lightweight and had some headings like so: Introduction, Goals, Non-goals, Overview, Detailed design, Security, Privacy, Testing. Compared to other design doc templates I've seen it wasn't heavy on software engineering theory. Of course the bulk of the writing would be in the "detailed design" section and subsections.
	- Good design docs were very detailed. One I wrote ended up being, I think, about 40 pages by the end when printed out, and that was not an especially large or unusual document. Design docs for critical systems could be larger still, or more frequently, split into many other docs. The quality of writing was generally high and they were maintained in version control. There was a mailing list where design docs were posted for company-wide review, though by the time I was there, this process had degraded quite a bit and a lot of stuff was done in team-specific design docs in Google Docs, with relatively minimal or no peer review. I felt that it was common for the less "serious" teams to do this, e.g. teams working on the latest chat product or on Google Apps itself. Those docs tended to be shorter, only partly filled out, or non-existent. The closer to the metal, older-school stuff was all hand-written HTML.
	- Good design docs would be kept up to date as the design evolved, although I'd say that was the minority. Most designs were the work of a small number of people or just one person. There were not many design review meetings that I recall, though probably that varied a lot by team.
	- Diagrams were minimal, possibly because there weren't any good diagramming tools available internally (well, there was graphviz and TeX).
	- Data structures would often be designed up front as long as they were either protocol buffers (i.e. inter-server comms or long term data storage), or fundamental to what the system did as with BigTable, indexing, index serving, ad serving etc. Systems where the data structures weren't fundamental to the design didn't necessarily plan out every structure in advance of course, by no means. For many products the user interface or network protocols were more important, so that's where the design docs would dwell.
	- The most senior engineers were very familiar with the performance costs of things, e.g. the cost of an L2 cache miss vs a disk seek, and that deeply informed the design of many systems.
	- That's about it.

**Facebook** moves fast and they don't have design docs, except few.
* The design process at Facebook is, to put it charitably, a bit minimal. "Move fast" is taken to mean start writing code immediately, then iterate on that to approach the desired outcome. Developers are <u>rewarded for landing code in production</u> each review period, even if that code provides little benefit, will need to be rewritten, and might even be buggy. In the rush, careful design and testing (which might delay landing in production and result in a bad review) get pretty short shrift. Some might say that there's risk or waste either way, and that <u>velocity rules all</u>. I'm not going to say they're wrong, but it makes "software design at Facebook" a bit of an oxymoron.
* In my experience working at Facebook, not a single thing you said was true.
	* People plan and think before they code.
	* People are rewarded for impact, not for landing useless code.
	* Code is carefully designed and tested, or it doesn't land.
	* Impact rules all, not velocity.
* Yeah. I worked in infra, so it could also be the difference between working on infra (where stability is valued) and working on product (where shipping fast is valued).

Ex Amazon here. **Amazon** has some solid principles that often go against popular belief.
- No waterfall-ish process where design is handed down from architects to senior engineers to juniors. The same people do design, implementation, ops and so on.
- Measure everything and always. People are encouraged to define metrics and goals and create dashboards before writing code
- Simplify: decreasing complexity is taken more seriously than in other companies. Do not use a database when you can use a file, or a message passing library when you can use a socket, or 200 lines of code when you can for out to "grep | sort". This can be surprising to new hires.