# Julia 超新手教學
Julia tutorials for dummy.

## Installation

### Install Julia

到 [官方下載頁面](https://julialang.org/downloads/) 下載目前穩定版（Current Release）。

請根據你的電腦作業系統以及位元版本下載相對應的安裝檔。

> Windows
>
> 直接點擊安裝檔~~無腦~~安裝。

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

* [1 簡介](/notebook/1_introduction.ipynb)
