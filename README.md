![CPP](https://img.shields.io/badge/Language-C++-blue?style=for-the-badge&logo=c%2B%2B)
![SFMLRequired](https://img.shields.io/badge/SFML-Required-red?style=for-the-badge&logo=sfml)

# SFPlot
A C++ Plot Library to be used in combination with SFML

# How to use
The file main.cpp provides an example of how to use this library

Create your data  
```c++
std::vector<double> data1 = {0, 50, 25, 17.5, 9, 4, 2, 1, 1, 1, 1};
DataSet set1(data1, sf::Color::Red);
```  
Create a SFPlot and plot your data  
```c++
SFPlot plotter(xax, "X Axo", "Y Axo", 50, &font);
plotter.plot(set1);
```  
Call setup, window is a sf::RenderWindow  
```
plotter.setup(&window, PlotType::Line);
```  
In your window loop:  
```
window.clear();
plotter.RenderTo(&window);
window.display();
```
## Example Plots
![Plot](img/graph1.png)
![Plot](img/graph2.png)
