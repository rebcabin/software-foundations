COQMFFLAGS := -Q . VFA  -arg "-w -omega-is-deprecated,-implicit-core-hint-db"

ALLVFILES := Preface.v Perm.v Sort.v Multiset.v BagPerm.v Selection.v Merge.v Maps.v SearchTree.v ADT.v Extract.v Redblack.v Trie.v Priqueue.v Binom.v Decide.v Color.v  PrefaceTest.v  PermTest.v  SortTest.v  MultisetTest.v  BagPermTest.v  SelectionTest.v  MergeTest.v  MapsTest.v  SearchTreeTest.v  ADTTest.v  ExtractTest.v  RedblackTest.v  TrieTest.v  PriqueueTest.v  BinomTest.v  DecideTest.v  ColorTest.v

build: Makefile.coq
	$(MAKE) -f Makefile.coq

clean::
	if [ -e Makefile.coq ]; then $(MAKE) -f Makefile.coq cleanall; fi
	$(RM) $(wildcard Makefile.coq Makefile.coq.conf) 

Makefile.coq:
	coq_makefile $(COQMFFLAGS) -o Makefile.coq $(ALLVFILES)

-include Makefile.coq

.PHONY: build clean
