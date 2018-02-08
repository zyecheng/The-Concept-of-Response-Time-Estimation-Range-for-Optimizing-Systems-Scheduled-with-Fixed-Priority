# The-Concept-of-Response-Time-Estimation-Range-for-Optimizing-Systems-Scheduled-with-Fixed-Priority

This repository contains the technical report and source code of our paper "The Concept of Response Time Estimation Range for Optimizing Systems Scheduled with Fixed Priority" submitted to RTAS 2018.


Abstract

Priority assignment is a critical issue in the design of real-time systems scheduled with fixed priority. In this paper, we consider the design optimization of a class of such real-time systems, where the schedulability of a task not only depends on the set of higher/lower priority tasks, but also on the response times of other tasks. This makes Audsley's algorithm inapplicable for finding a schedulable priority assignment, not to mention that the design optimization may also involve other metrics such as end-to-end latency in the constraints or objective. The current approaches are to either develop heuristics or use standard exhaustive search algorithms such as Branch-and-Bound (BnB).

Instead, we propose a new approach that breaks through the mindset of the current approaches. Our main idea is to introduce the concept of response time estimation range, which is used in place of the actual response time of each task for evaluating the system schedulability. This allows to leverage Audsley's algorithm to generalize from an unschedulable solution to many similar ones. We develop an optimization framework that builds upon such a concept.
%
We then apply the proposed approach to industrial designs of two use cases. One is the real-time wormhole communication in a Network-on-Chip (NoC), where a traffic flow suffers indirect interferences that depend on the response times of higher priority flows. The other is distributed systems with data-driven activation, where a task is triggered by the availability of data, hence by the completion of its immediate predecessor. Experimental results show the proposed technique typically runs several times faster than exhaustive search algorithms based on BnB or Mixed Integer Linear Programming (MILP).
