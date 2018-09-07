# Julia 超新手教學
Julia tutorials for dummy.

## Installation

### Install Julia

到 [官方下載頁面](https://julialang.org/downloads/) 下載目前穩定版（Current Release）。

請根據你的電腦作業系統以及位元版本下載相對應的安裝檔。

> Windows
>
> 直接點擊安裝檔~~無腦~~安裝。

> macOS
>
> 安裝好後，應該可以在 `/Applications` 找到 `Julia-<version>.app` (最新版是 `1.0.0`)
> 點擊兩下應該會開啟 Terminal 並進入 `julia` 的 consule
>
> 如果你跟我一樣不喜歡用觸控板點點點，比較喜歡打字
> 可以考慮在 `~/.bash_profile` 中加入這一小段
```{bash}
_setup_julia(){
    if [ "$(uname -s)" != 'Darwin' ]; then
        echo 'julia setup function works only on macOS';
        return 2;
    fi; 
    JULIA_APP="$(command ls /Applications | grep -i julia | sort -r | head -1)";
    if [ ! "${JULIA_APP}" ]; then
        echo "Julia is not installed";
        return 1;
    fi; 
    JULIA_PATH="/Applications/${JULIA_APP}/Contents/Resources/julia/bin";
    export PATH=$PATH:$JULIA_PATH;
    unset JULIA_APP JULIA_PATH;
}
_setup_julia
unset _setup_julia
```
> 之後開一個新的 Terminal 起來，直接執行 `julia`，
> 應該就可以看到最新版的 `julia` consule


### Test Julia

> Windows
>
> 左下方"開始" > "Julia 1.0.0" > "julia-1.0.0"

### Install Jupyter

建議安裝 [Anaconda](https://www.anaconda.com/download/)，請選擇 Python 3.6 的版本安裝。

當中內建 Jupyter 不需額外安裝。

### Install IJulia

> Windows
>
> 左下方"開始" > "Julia 1.0.0" > "julia-1.0.0"
>
> 會進入 Julia 的互動式命令介面
>
> 打入 `Pkg.update()` 做套件更新，請確定你有連上網路
>
> 打入 `Pkg.add("IJulia")` 安裝 IJulia。

### Test IJulia

> 安裝成功後，打入 `using IJulia`
>
> 打入 `notebook()` 開啟 Jupyter

## Usage

### 開啟 Jupyter notebook 來執行 julia

> Windows
>
> 左下方"開始" > "Julia 1.0.0" > "julia-1.0.0"
>
> 會進入 Julia 的互動式命令介面
>
> 打入 `using IJulia`
>
> 打入 `notebook()` 開啟 Jupyter

## Contents

### Notebooks

* [1 簡介](/notebook/1_introduction.ipynb)
* [2 組織起來吧！](/notebook/2_organize_it.ipynb)
* [3 型別系統](/notebook/3_types.ipynb)
* [4 方法](/notebook/4_methods.ipynb)

### Slides

* [1 簡介](/slides/1_introduction.slides.pdf)
* [2 組織起來吧！](/slides/2_organize_it.slides.pdf)
* [3 型別系統](/slides/3_types.slides.pdf)
* [4 方法](/notebook/4_methods.slides.pdf)
