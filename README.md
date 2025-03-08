# numpy3-pd1
numpy and panda

numpy continue shift+tab= to see the help of the function

ones()- creates array with 1 values, dtype default=float
functions on images: same functionality works on array of numbers:
from skimage import io
photo=io.imread('image path') # same path of the notbook or, full path
convert the image to 2d array- shape=tuple (legth,numbers)
each cell contain the cell colors the rgb colors
to view the photo:
  import matplotlit.pylot as plt
  plt.imshow(photo)
np.where(photo>100,255,0)#for each cell set 255 if true, else set 0
plt.imshow(photo.transpose(1,0,2) # y1,x0,z2)# rotate the image
another option import pil to rotate the photo by degrees
# Imports PIL module
from PIL import Image
# open method used to open different extension image file
im = Image.open(r"C:\Users\System-Pc\Desktop\ybear.jpg")

# This method will show image in any image viewer
im.show()
plt.imshow(photo[:,150,:]),
to reverse=photo[::-1]
np.std(arr)= סטית תקן
np.var= שונות, different for the agv
np.mean(arr)= חציון,avg
np.full(dim,value)= create array with init given value
arr1/arr2= must be same length
np.power(arr,2)# for each item^2
arr3=append(arr1,arr2) # create new array with concat the 2 arrays.
arr4=insert(arr3,index,value)=return new array with add in given index the value, and push the others. img.png
can override the exist array
if not override, doesn't change the origin array.
delete(arr4,0)= return the new array without the deleted value.
doesn't change the origin array, if you don't override it.
axis=על איזה ציר אתה רוצה את הפעולה :
if the array is more than 1d, can define on what column to make the action:
arr.sum(axis=None)= arr.sum()= default= return the sum of all values in the arr
arr.sum(axis=0) = sum of all values:
arr.sum(axis=1)
impletmentation to explain:
axis=0
for col in range
  for row in range
     sum=arr[row][col] axis=0
axis=1
for row in range
   for col in range
    sum=arr[row][col] axis=1
Pandas Library: an open source data manipulation and analysis in python code languages.
provides flexible data structures for fast and efficient manipulations.
will work mainly in data structures of series,dataframe type
usages:
Data Wrangling and Cleaning= organize and clean the data
Statistical Analysis
Working with Different Data Sources: allow to work wide various sources
Series : a dictionary with static locations of the (key, value)- like a numpy array
the key called index
to create Series: pd.Series(data, indexes):
data is an array, indexes=default and None- and the created key will be autoincrement from 0
the created Series built from index(key), value
another way to create Series, simple create a dictionary with {keys: values}
access values is like in np.array: pd_Series[start/index:end:jump], pd_Series[0],pd_Series[0::2]
pd_Series[0]- get error on deprecated, need to use dp_Series.iloc(0)
type(pd_Series)= the type of the values in the Series
reset_index:to reset indexes: pd_Series.reset_index(drop=True)- doesn't change the origin,return a new Series with new indexes as autoincrement values
pd_Series.reset_index(drop=True, inplace=true)= will change the origin Series
assign indexes instead the exist ones: pd_Series.index=['usa',...]
reindex()- change the location of the indexes, the indexes must be exist in the Series.
pd_Series.keys(): get all keys- vs pd_Series.index(return array like from Index type).
pd_Series.values=get all values- as a simple array/list
access by key: pd_Series['usa']
Series addition operator: to concat Series: kind of full join 2 Series.
with operator +: if has same key(match): will merge the value, else set key:None
first.add(second,fillvalue if no match)
