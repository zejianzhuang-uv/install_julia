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
juliaup add release
```



## Using package from Python
```julia
ENV["PYTHON"] = ""
```
