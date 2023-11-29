@def title = "My Franklin Example"
@def tags = ["syntax", "code"]


# Hola 
\toc

## Plotly
```julia:ex1
using PlotlyJS
z =  [10     10.625  12.5  15.625  20
     5.625  6.25    8.125 11.25   15.625
     2.5    3.125   5.    8.125   12.5
     0.625  1.25    3.125 6.25    10.625
     0      0.625   2.5   5.625   10]

data   = contour(; z=z)
layout = Layout(; title="Basic Contour Plot")
plt    = plot(data, layout)

fdplotly(json(plt)) # hide
```
\textoutput{ex1}

## plty2
```julia:ex2
using PlotlyJS
p=plot(
     scatter(x=1:10, y=rand(10), mode="markers"),
     Layout(title="Responsive Plots")
     )
savejson(p, joinpath(@OUTPUT, "plotlyex.json"))  # savejson is an alternative to savefig # hide
# PlotlyBase.json (also exported by PlotlyJS) often gives a smaller json compared to PlotlyJS.savefig # hide
```

\fig{plotlyex}


## teble of contents

Texto x para mostrar

$$ 7 + 5 = 546 $$

$$ 5+655 65 4 $$


## Using Julia

```julia:./ex11
println("HelloWorld")

```

\show{./ex11}


## 
