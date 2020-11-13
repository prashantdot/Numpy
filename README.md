# Write a function to find moving average in an array over a window:
# Test it over [3, 5, 7, 2, 8, 10, 11, 65, 72, 81, 99, 100, 150] and window of 3.



def mov_avg_val(mylist, N):
    cumsum, moving_aves = [0], []
    for i, x in enumerate(mylist, 1):
        cumsum.append(cumsum[i-1] + x) # summing up all the values one by one and appending the list
        if i>=N:
            moving_ave = round(((cumsum[i] - cumsum[i-N])/N),2) #computing the moving average using temp array sum array cumsum
            #can do stuff with moving_ave here
            moving_aves.append(moving_ave) # listing the moving average as an single array
    print("Moving average values list: ", moving_aves)
    print("Length of the list l-N+1: ", len(moving_aves))
