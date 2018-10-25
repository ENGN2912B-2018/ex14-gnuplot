# Gnuplot graphics plotting utility

Gnuplot is a powerful plotting utility for 2D and 3D graphics.  Many of the typcial plots found in MATLAB can be replicated using Gnuplot.  By itself, however, Gnuplot is a standalone program and cannot interface directly with a C++ program.

## Gnuplot-iostream interface library

Several 3rd party projects have been created as solutions to use gnuplot as a simple, easy-to-use plotting tool that accepts C++ vectors and multi-dimensional data types.  This is where the gnuplot-iostream library comes into play.

The iostream interface uses the `<<` operator to pass data and commands directly to an instance of a Gnuplot object.  Two working examples are found in the `src` directory that were adopted from the author's web page.

## Compiling programs with the Gnuplot-iostream interface

Gnuplot-iostream uses Boost and therefore requires including the Boost.Iostreams library.

