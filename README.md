# Install Julia
## Using `juliaup`
Seting a path to store julia version and configuration file
```sh
echo 'export JULIAUP_DEPOT_PATH=/opt/' >> ~/.zshrc
source ~/.zshrc
```
Install `juliaup` by homebrew
```sh
brew install juliaup
#or
curl -fsSL https://install.julialang.org | sh
juliaup add release
```



## Using package from Python by `PyCall` and `PythonCall`
- Create a folder called `config` under the `~/.julia/`
- Create a new file call `startup.jl` and fill the below:
```julia
# ENV["JULIA_CONDAPKG_BACKEND"] = "Null"
ENV["PYTHON"] = "/opt/anaconda3/envs/JuliaPy/bin/python"
ENV["JULIA_CONDAPKG_BACKEND"] = "Null"
# ENV["JULIA_PYTHONCALL_EXE"] = "/opt/anaconda3/envs/JuliaPy/bin/python"
# ENV["JULIA_PYTHONCALL_EXE"] = "@PyCall"  # optional
ENV["IJULIA_PYTHONCALL"] = "0"
```
- Install `PyCall` and `PythonCall`
