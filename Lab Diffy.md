import random 

text = open('text.txt', 'w+') 

P = random.randint(3, 100) 
print('Random number for P = ', P) 
text.write('Random number for P = ' + str(P) + '\n') 

A = random.randint(3, P) 
print ('Random number for A = ', A) 
text.write('Random number for A = ' + str(A) + '\n') 

print('Alice message -> Bob') 
X1 = int(input()) 
text.write('Alice message -> Bob ' + str(X1) + '\n') 

print('Bob message -> Alice') 
X2 = int(input()) 
text.write('Bob message -> Alice ' + str(X2) + '\n') 

Y1 = (A**X1)%P 
text.write("Alice's key " + str(Y1) + '\n') 
Y2 = (A**X2)%P 
text.write("Bob's key " + str(X2) + '\n') 

N = (Y2**X1)%P 
M = (Y1**X2)%P 

text.write('Results ' + str(N) + ' ' + str(M) + '\n') 
print('Results ', N, M) 
text.close()
