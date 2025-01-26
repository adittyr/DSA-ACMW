def permutations(res, arr, idx):
    if idx == len(arr) - 1:
       res.append(arr[:])
       return 
    for i in range(idx, len(arr)):
        arr[idx], arr[i] = arr[i], arr[idx]
        permutations (res, arr, idx +1) 
        arr[idx], arr[i] = arr[i], arr[idx] 
def next_permutation(arr):
   curr = arr[:]
   res = []
   permutations(res, curr, 0)
   res.sort()
   for i in range(len(res)):
       if res[i] == arr:
          if i < len(res) -1:
               arr[:] = res[i+1]
          else:
               arr[:] = res[0]
          break 
if __name__ == "__main__":
   arr = [2, 4, 1, 7, 5, 0]
   next_permutation(arr)
   print("".join(map(str, arr)))
