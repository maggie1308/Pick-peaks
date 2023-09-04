'''
In this kata, you will write a function that returns the positions and the values of the "peaks" (or local maxima) of a numeric array.

For example, the array has a peak at position with a value of (since equals ).arr = [0, 1, 2, 5, 1, 0]35arr[3]5

The output will be returned as an object with two properties: pos and peaks. Both of these properties should be arrays. 

If there is no peak in the given array, then the output should be .{pos: [], peaks: []}

Example: should return (or equivalent in other languages)pickPeaks([3, 2, 3, 6, 4, 1, 2, 3, 2, 1, 2, 3]){pos: [3, 7], peaks: [6, 3]}

All input arrays will be valid integer arrays (although it could still be empty), so you won't need to validate the input.

The first and last elements of the array will not be considered as peaks (in the context of a mathematical function, 
we don't know what is after and before and therefore, we don't know if it is a peak or not).

Also, beware of plateaus !!! has a peak while and do not. In case of a plateau-peak, please only return the position and value of the beginning of the plateau.
For example: returns (or equivalent in other languages)[1, 2, 2, 2, 1][1, 2, 2, 2, 3][1, 2, 2, 2, 2]pickPeaks([1, 2, 2, 2, 1]){pos: [1], peaks: [2]}
'''

def pick_peaks(arr):
    peaks =[]
    pos=[]
    flag = False
    findex = None
    ffirst = None
    for i in range(1, len(arr) - 1):
        if arr[i - 1] < arr[i] > arr[i + 1]:
            pos.append(i)
            peaks.append(arr[i])
        if arr[i - 1] < arr[i]  and arr[i] == arr[i + 1]:
            flag = True
            findex = i 
            ffirst = arr[i]
        if arr [i - 1] == arr[i] and arr[i] > arr[i + 1] and flag:
            pos.append(findex)
            peaks.append(ffirst)
            flag = False       
    return  {"pos":pos,"peaks":peaks}
