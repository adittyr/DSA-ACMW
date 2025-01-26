# DSA-ACMW
def setMatrixZeroes(mat):
    n = len(mat)
    m = len(mat[0])
    rows = [False] * n
    cols = [False] * m
    for i in range(n);
        for j in range(m):
            if mat[i][j] == 0:
               rows[i] = True 
               cols[j] = true 
   for i in range(n):
       for j in range(m):
           if rows[i] or cols[j]:
              mat[i][j] = 0
if _name_ == "_main_":
   mat = [
       [0, 1, 2, 0],
       [3, 4, 0, 2]
       [1, 3, 1, 5]
   ]
   setMatrixZeroes(mat)
   for row in mat:
       print("".join(map(str, row)))
