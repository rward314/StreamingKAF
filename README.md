# StreamingKAF

Scalable Kernel Analog Forecasting (Scalable-KAF)

Based on the algorithm described in
D. Giannakis, A. Henriksen, J. Tropp, R. Ward, Learning to Forecast Dynamical Systems from Streaming Data, Preprint, 2021.

Comments are welcome.
This is the first version of the toolbox and may not be as robust or well-documented as it should be. Please keep track of bugs or missing/confusing instructions and report them to us.

MIT License

COPYRIGHT (c) 2021 by  
Dimitris Giannakis  <dimitris(at)cims.nyu.edu>, Courant Institute, NYU
Amelia Henriksen <amelia@ices.utexas.edu>, UT Austin 
Rachel Ward <rward@math.utexas.edu>, UT Austin
Joel Tropp  <jtropp@caltech.edu>, Caltech

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies
of the Software, and to permit persons to whom the Software is furnished to do
so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.


------------------------------------

Files included:

driver.m    		This is the code that the user should run to test the timing and performance of
                  		Scalable-KAF on various examples 

TwoPhaseLorenz.m   This function (which calls L96fcn.m) generates trajectory data from the two-phase 		   Lorenz 96 dynamical system 

L96fcn.m		Evolves the Lorenz96 system forward by one time step

Lorenz63.m		This function generates trajectory data for the Lorenz63 dynamical system

ScalableKAF.m	This class is the main code for training ScalableKAF.  

RFF.m			This class is a feature map for Gaussian RBF kernel. 

ForecastModel.m     This class uses ScalableKAF + observable data to construct a nonlinear 			forecasting model

FeatNystrom.m	This function computes a truncated eigenvalue decomposition of featured data 
			by streaming over the columns  

GaussRBF.m		This class implements the Gaussian RBF kernel

subplus.m		This function returns the positive part of an array of real numbers

NaiveKAF.m		This class uses the Gaussian RBF kernel to predict observations from state data

NaiveForecastModel.m	This class uses NaiveKAF + observable data to construct a nonlinear 
				forecasting model  









			

      








