## Boa: A Language and Infrastructure for Analyzing Ultra-Large-Scale Software Repositories

```
1 rates: output mean[string] of int ;
2 p: Project = input ;
3 foreach (i : int ; p.code_repositories[i ]. kind == RepositoryKind.SVN
          && len(p. code_repositories[i].revisions) > 10)
4   exists ( j : int ; match(‘^java$‘, lowercase(p.programming_languages[j])))
5     foreach (k: int ; len(p.code_repositories[i ]. revisions [k ]. files ) < 100)
6        rates[p.id ] << len(p.code_repositories[i ]. revisions [k ]. files ) ;
```
- On line 1, this program declares an output called rates, which collects integer values and produces a final result by aggregating the input values for each project (indexed by a string) using the function mean.
- On line 2, it declares that the input to this program will be a project, e.g. Apache OpenOffice. Boa’s infrastructure manages the details of downloading projects and their associated information.
- For each project, the code on lines 3–6 runs. If a repository contains 600k projects, the code on lines 3–6 runs for each.
-

### Boa Language

- Domain-Specific Types in Boa
- MapReduce Support
- Quantifiers
- User_Defined Functions in Boa


### Compiler and Runtime

- Sizzle compiler, open-source Java implementation of the Sawzall language.
- implementation efforts
  - User_Defined Functions
  - Quantifiers
  - Protocol Buffers (Protocol buffers are a data description format developed by Google that are stored as binary messages.)


### Supporting data Infrastructure

- monthly snapshots
- convert the data into the format required by our framework
- Web-Based Interface

### Evaluation

**research questions**
1. Applicability
2. Scalability
  - scaling the size of the cluster and
  - scaling the size of the input.
3. Reproducibility
