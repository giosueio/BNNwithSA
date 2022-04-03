# Fitting Binary Neural Networks with Simulated Annealing
Using Simulated Annealing (SA) to train multiclass classification feedforward Neural Networks with weights and activations constrained to +1 and -1, aka Binary Neural Networks (BNNs).

## Repository structure

The two main `Julia` scripts are in `src/`:
| Script  | Description |
| ------------- | ------------- |
| `BNN.jl`  | Contains structs and functions defining the core of the BNN implementation and of SA optimization procedure  |
| `BNN_operators.jl`  | Contains some ancillary function implemented to ease notation & computation |

<br />

`BNN_analysis.jl` contains some additional functions used to analyze weight configurations obtained with the algorithm.
<br />

| Function  | Description |
| ------------- | ------------- |
| solution_landscape  | Change at random an increasing portion of the weight matrix, see how error on the trainin set changes consequentially  |
| test_layer_elements  | For a given number of layers H, plot how the error changes on the training set as more units are added to each layer |
| test_number_layers  | For a given number of units M per layer, plot how the error changes on the training set as more layers are added  |
<br />

The presentation `Algorithms_Project(7).pdf` presents tests on two datasets:
- **Breast Cancer Wisconsin** dataset for binary classification
- **Iris** dataset for multiclass classification

## Quick start

Clone the repo, `cd` the project's folder and install the depencies by running on `Julia`
```
pkg> activate .
(BNN) pkg> instantiate
```
One can then access the repo's methods by specifying

```
(BNN) julia> using BNN
(BNN) julia> include("BNN_analysis.jl") 

```


## Credits
Project by Giosuè Migliorini ([giosue.migliorini@gmail.com](mailto:giosue.migliorini@gmail.com)) as part of the course [20602 - COMPUTER SCIENCE (ALGORITHMS)](https://didattica.unibocconi.eu/ts/tsn_anteprima.php?cod_ins=20602&anno=2021&IdPag=6164), taught by professors C.Feinauer and F.Pittorino.
Reference to relevant literature on the topic can be found in `Algorithms_Project(7).pdf`
