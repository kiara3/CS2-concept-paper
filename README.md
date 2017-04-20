# CS2-concept-paper
\documentclass{article}

\title{PARALLEL VERSION OF TARJAN'S ALGORITHM}
\author{NSEREKO NICODEMUS   15/U/22184     215023556,    }
\begin{document}

\maketitle
\section{Introduction}{In this paper is the concurrent version of algorithms based on depth-first search, all variants of Tarjan’s Algorithm namely; finding the strongly connected components (SCCs) of a graph, finding which nodes are part of the cycle in the graph, and finding which nodes are part of a “lasso”( such that there is a path from the node to a node on a cycle).}
\subsection{Background}{We basically aim at building concurrent algorithms based on depth-first search \cite{ref2} for the three problems relevant to model checking; finding its strong connected components states that are in loops, those in lassos. : If we have more than one processor at our disposal, we can solve a problem more quickly by dividing it into independent sub-problems and solving them at the same time, one on each processor.}

{We present concurrent algorithms for each of the above three problems. Our implementations typically exhibit about a four-fold speed-up over the corresponding sequential algorithms on an eight-core machine; the speed-ups are slightly better on graphs with a higher ratio of transitions to states. }

\subsection{Problem statement}{It is quite hard to import Tarjan’s algorithm in a parallel manner since according to its implementations; it uses a depth first search(DFS) which doesn’t explore already explored nodes. The strongly connected components then form subtrees of the search tree. The nodes are placed on a stack as they are visited. When the search returns from the subtree, the nodes are popped off the stack and checked to see if they are a root of a strongly connected component. If the node is a root, then it and all the nodes taken off before it form the strongly connected component.}
\end{document}
