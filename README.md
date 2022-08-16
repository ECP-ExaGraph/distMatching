# distMatching

A b-MATCHING is a subset of edges M such that at
most b(v) edges in M are incident on each vertex v, where b(v) is
specified. We present a distributed-memory parallel algorithm,
b-SUITOR, that computes a b-MATCHING with more than half
the maximum weight in a graph with weights on the edges. The
approximation algorithm is designed to have high concurrency
and low time complexity. We organize the implementation of
the algorithm in terms of asynchronous supersteps that combine
computation and communication, and balance the computational work and frequency of communication to obtain high
performance. Since the performance of the b-SUITOR algorithm
is strongly influenced by communication, we present several
strategies to reduce the communication volume. We implement
the algorithm using a hybrid strategy where inter-node communication uses MPI and intra-node computation is done with
OpenMP threads. We demonstrate strong and weak scaling of
b-SUITOR up to 16K processors on two supercomputers at
NERSC. We compute a b-MATCHING in a graph with 2 billion
edges in under 4 seconds using 16K processors.

Citation:

@inproceedings{khan2016designing,
  title={Designing scalable b-matching algorithms on distributed memory multiprocessors by approximation},
  author={Khan, Arif and Pothen, Alex and Patwary, Md Mostofa Ali and Halappanavar, Mahantesh and Satish, Nadathur Rajagopalan and Sundaram, Narayanan and Dubey, Pradeep},
  booktitle={SC'16: Proceedings of the International Conference for High Performance Computing, Networking, Storage and Analysis},
  pages={773--783},
  year={2016},
  organization={IEEE}
}
