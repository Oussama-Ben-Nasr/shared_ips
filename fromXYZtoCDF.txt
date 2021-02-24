# this code is only converting X,Y,Z error to a CDF error
# this will work as helper code to evaluate algorithms
# depandancy matpltlib.pyplot, numpy

import numpy as np
import matplotlib.pyplot as plt
from random import randint

def visualizeErrorAxis(X_true,X_predicted):
	plt.plot(np.sort(np.sqrt(X_true**2+ X_predicted**2)),np.array(range(len(X_true)))/(len(X_true)))
	plt.show()
def testVisualizeErrorAxis(N,visualizeErrorAxis):
	X=np.array([randint(0,1000) for i in range(N)])
	Y=np.array([randint(0,1000) for i in range(N)])
	print(X*X)
	print(np.sqrt(X*X))
	
	print("Testing visualizeErrorAxis with two {} values vectors".format(N))
	visualizeErrorAxis(X,Y)
	return 0
if __name__=="__main__":
	N=10000
	#testVisualizeErrorAxis(N,visualizeErrorAxis) # test passed successfully	