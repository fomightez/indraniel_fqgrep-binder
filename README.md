
# indraniel_fqgrep-binder
Analysis of sequencing data using indraniel/fqgrep, *an approximate sequence pattern matcher for FASTQ/FASTA files*, in Jupyter sessions provided via MyBinder.org. Adapt the demonstrations to analyze your data and create reports.

[![Binder](https://mybinder.org/badge_logo.svg)](https://mybinder.org/v2/gh/fomightez/indraniel_fqgrep-binder/HEAD?urlpath=%2Flab%2Ftree%2FDemonstrate+indraniel+fqgrep.ipynb)


*tl;dr:*  
Click any `launch binder` badge on this page to use the demonstrations inside your browser.

See [the source repo for Indraniel Das' fqgrep here](https://github.com/indraniel/fqgrep) for more about the software.

**Note if you are interested in this software, see [my fqgrep-binder repo](https://github.com/fomightez/fqgrep-binder) where I demonstrate Fulcrum Genomics' fqgrep, and I also mention Patmatch which belongs in discussions of this sort of software. However, Patmatch only works with FASTA files.**

------------------

You more likely are interested [Fulcrum Genomics' fqgrep](https://github.com/fulcrumgenomics/fqgrep)!! It is much more current and better maintained than [Indraniel Das' fqgrep here](https://github.com/indraniel/fqgrep).  
I have a nice demonstration site for Fulcrum Genomics' fqgrep that you can easily run via MyBinder-served sessions without installing anything on your machine, see [my fqgrep-binder repo](https://github.com/fomightez/fqgrep-binder).


------------------

## Related utilities

- Fulcrum Genomics' fqgrep

	Fulcrum Genomics' fqgrep is more developed and in some ways more full-featured than Indraniel Das' fqgrep.
	See more about it and try it in MyBinder-served sessions [here](https://github.com/fomightez/fqgrep-binder).  
	My understanding is that is more restrictive than Indraniel Das' fqgrep in how you can specify mismatches, at this time.

- seqkit grep
	[seqkit grep](https://bioinf.shenwei.me/seqkit/usage/#grep) appears to allow biological-type mismatches and since it is part of a 'Utrafast FASTA/Q kit', I assume it works on both file formats. I have yet to try it. Learned of it from [this Biostar's post](https://www.biostars.org/p/346852/#346875) when I thought to include 'fuzzy' as a search term when I was pondering why no one cared that Fulcrum Genomics' fqgrep seems not to support biologica-style mismatches or Indraniel Das' fqgrep is not maintained.

- Patmatch

	[Patmatch](https://github.com/fomightez/patmatch-binder) will run on FASTA to find matches to patterns. Patmatch supports IUPAC and mismatch insertions, deletions, and substitutions that I haven't seen Fulcrum Genomics' fqgrep support. 

	And so if you need to allow mismatches with numbers of insertions, deletions, and substitutions, see more about Patmatch [here](https://github.com/fomightez/patmatch-binder).


