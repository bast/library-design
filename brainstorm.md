# Library Design the Hard Way

Radovan Bast and Roberto Di Remigio

## Brainstorming

* I think it is safe to say that we have accumulated some experience in transitioning from monolithic code bases to modular ones. What are the lessons we can distill from this? Are these generally applicable? Are these known from software engineering?

* Are the lessons learnt equally applicable across different programming languages?

* Is there friction in between good design and good performance? And do we need to discuss this point?

* Are there any lessons one can learn from purely functional programming? Are _Out of the Tar Pit_ and _The Curse of the Excluded Middle_ relevant literature?

* Obsolescence and refactoring. Planning for change, both as extensibility and as updating/upgrading for new programming techniques. For example, OpenMP (OpenACC) parallelization of existing code.

## Resources

### Online

* [How to Design a Good API and Why it Matters](http://landawn.com/How%20to%20Design%20a%20Good%20API%20and%20Why%20it%20Matters.pdf)

* [The Little Manual of API Design](http://people.mpi-inf.mpg.de/~jblanche/api-design.pdf)

* [Beautiful Native Libraries](http://lucumr.pocoo.org/2013/8/18/beautiful-native-libraries/)

* [Library Design the Hard Way](https://github.com/bast/talk-library-design)

* [Context-aware API example](https://github.com/bast/context-api-example)

### Books

*_Nicklaus Wirth_, Algorithms + Data Structures =  Programs

*_Erich Gamma, Richard Helm, Ralph Johnson, John Vlissides_ Design Patterns

* _Martin Reddy_, API Design for C++

### Papers

* Dijkstra, Edsger W. 1968. _The Structure of the ‘THE’-Multiprogramming System_ **Communications of the ACM** 11 (5). ACM: 341–46. doi:10.1145/363095.363143.

* Parnas, D. L. 1972. _On the Criteria to Be Used in Decomposing Systems into Modules_ **Communications of the ACM** 15 (12). ACM: 1053–58. doi:10.1145/361598.361623.

* Wilson, Greg, D. A. Aruliah, C. Titus Brown, Neil P. Chue Hong, Matt Davis, Richard T. Guy, Steven H. D. Haddock, et al. 2014. _Best Practices for Scientific Computing_ **PLoS Biology** 12 (1): e1001745. doi:10.1371/journal.pbio.1001745.

* Seeley, Donn 2004. _How Not to Write Fortran in Any Language_ **Queueing Systems. Theory and Applications** 2 (9). ACM: 58–65. doi:10.1145/1039511.1039535.

* Stodden, Victoria, and Sheila Miguez. 2014. _Best Practices for Computational Science: Software Infrastructure and Environments for Reproducible and Extensible Research_ **Journal of Open Research Software** 2 (1): e21. doi:10.5334/jors.ay.

## Dicta

These are some "rules" or "practical guiding principles" one might want to keep in mind at all stages in library development:

* For any high-level construct introduced, is there a way to bypass it and use the lower level construct(s) it is supposed to wrap?

* Extensibility by third-parties is more important than extensibility by the library writers/maintainers.

