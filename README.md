# Rexl Sample Notebooks

This repository holds sample Jupyter notebooks and associated data for the
[Rexl project](https://github.com/microsoft/Rexl).

## Contents

* [Releases](#releases)
* [Samples](#samples)
* [Contributing](#contributing)
* [Trademarks](#trademarks)

## Releases

We will publish releases of the Rexl sample notebooks (and data) here in GitHub.
A release consists of a `.zip` file containing the notebooks and data. To use:

* Ensure that a release of the `RexlKernel` has been properly installed, as described in
  the [Rexl README](https://github.com/microsoft/Rexl#Releases).
* Download the `RexlSampleNotebooks.zip` file.
* Extract the contents of the `.zip` to a folder.
* Open a command line shell and `cd` into the extracted folder.
* Run `jupyter lab`.
* In Jupyter Lab, you should see directories named `notebooks` and `data`, containing the sample
  notebooks and data. You should also see an icon for creating a new `Rexl` notebook.

## Samples

The `samples` directory contains the directories
* [notebooks](#notebooks)
* [data](#data)

### Notebooks

The [notebooks](/samples/notebooks) directory contains Jupyter notebook files. To run the notebooks,
ensure that Jupyter is properly installed and that the Rexl kernel is built and registered.

The Jupyter notebook files include:
* [NFL.ipynb](/samples/notebooks/NFL.ipynb): demonstrates some tabular data manipulation using NFL game data.
* [Comma.ipynb](/samples/notebooks/Comma.ipynb): discusses the _implicit lambda_ pattern and why Rexl doesn't
  need an analog of Excel's `SUMPRODUCT` function.
* [ImageAsTensor.ipynb](/samples/notebooks/ImageAsTensor.ipynb): Illustrates representing images as tensors
  and performing some basic transformation.
* [ImageClassification.ipynb](/samples/notebooks/ImageClassification.ipynb): Illustrates using some ONNX
  models from Rexl to classify images.
* [ProteinFolding.ipynb](/samples/notebooks/ProteinFolding.ipynb): Illustrates a protein folding optimization
  problem formulated as a Rexl module. Solves using three integrated MIP solvers,
  [Gurobi](https://www.gurobi.com/) (requires license), [HiGHS](https://highs.dev/), and
  [GLPK](https://www.gnu.org/software/glpk/).
* [EssentialMedicines.ipynb](/samples/notebooks/EssentialMedicines.ipynb): Uses Rexl _module_ functionality
  to formulate an essential medicines optimization problem. Rexl dispatches to the Gurobi solver
  (requires license from Gurobi) to perfom the optimization.
* [HoneycombPuzzleSat.ipynb](/samples/notebooks/HoneycombPuzzleSat.ipynb): Illustrates using the SAT
  (boolean satisfiability) solver to find solutions to a tricky geometric puzzle.
* [SudokuSat.ipynb](/samples/notebooks/SudokuSat.ipynb): Uses the Rexl SAT solver to solve Sudoku puzzles.
* [SudokuMip.ipynb](/samples/notebooks/SudokuMip.ipynb) and
  [SudokuMipEq.ipynb](/samples/notebooks/SudokuMipEq.ipynb.ipynb):
  These use Rexl _module_ functionality and MIP solver integration to solve Sudoku puzzles.

### Data

The [data](/samples/data) directory contains data files of various forms used in the sample notebooks.
Some of the files are Rexl scripts that define one or more global symbols. Other files may be binary
data files (such as parquet or rbin files) or images (jpg, png) or just about anything.

The data files include:
* [NFL-2010-Games.rexl](/samples/data/NFL-2010-Games.rexl):
  A RexlScript file that defines a global named `Games` containing data for the NFL games played during the
  2010 regular season.
* [Orders.rexl](/samples/data/Orders.rexl): A RexlScript file
  that defines a global named `Orders` containing (fictitious) data for customer orders.
* [ChemNodes.rbin](/samples/data) and [ReacNodes.rbin](/samples/data): These are the tables needed for the
  [EssentialMedicines.ipynb](/samples/notebooks/EssentialMedicines.ipynb) notebook.
* [HoneycombPuzzlePieces.jpeg](/samples/data/HoneycombPuzzlePieces.jpeg) and
  [HoneycombPuzzleSolution.jpeg](/samples/data/HoneycombPuzzleSolution.jpeg): These are images used in the
  [HoneycombPuzzleSat.ipynb](/samples/notebooks/HoneycombPuzzleSat.ipynb) notebook.
* [HoneycombPuzzleSlns.rbin](/samples/data/HoneycombPuzzleSlns.rbin): This contains the solutions generated
  by the [HoneycombPuzzleSat.ipynb](/samples/notebooks/HoneycombPuzzleSat.ipynb) notebook.

 **Note**: when adding a new kind of data file that should use LFS (large file storage), ensure that the
 [`.gitattributes`](/.gitattributes) file has an entry for the extension.

## Contributing

This project welcomes contributions and suggestions.  Most contributions require you to agree to a
Contributor License Agreement (CLA) declaring that you have the right to, and actually do, grant us
the rights to use your contribution. For details, visit https://cla.opensource.microsoft.com.

When you submit a pull request, a CLA bot will automatically determine whether you need to provide
a CLA and decorate the PR appropriately (e.g., status check, comment). Simply follow the instructions
provided by the bot. You will only need to do this once across all repos using our CLA.

This project has adopted the [Microsoft Open Source Code of Conduct](https://opensource.microsoft.com/codeofconduct/).
For more information see the [Code of Conduct FAQ](https://opensource.microsoft.com/codeofconduct/faq/) or
contact [opencode@microsoft.com](mailto:opencode@microsoft.com) with any additional questions or comments.

## Trademarks

This project may contain trademarks or logos for projects, products, or services. Authorized use of Microsoft 
trademarks or logos is subject to and must follow 
[Microsoft's Trademark & Brand Guidelines](https://www.microsoft.com/en-us/legal/intellectualproperty/trademarks/usage/general).
Use of Microsoft trademarks or logos in modified versions of this project must not cause confusion or imply Microsoft sponsorship.
Any use of third-party trademarks or logos are subject to those third-party's policies.
