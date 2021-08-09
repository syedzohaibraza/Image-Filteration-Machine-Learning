def aman_effect(data, filter_size):
  temp = []
  indexer = filter_size // 2
  new_image = data.copy()
  nrow, ncol = data.shape
  for i in range(nrow):
    for j in range(ncol):
      for k in range(i-indexer, i+indexer+1):
        for m in range(j-indexer, j+indexer+1):
          if (k &gt; -1) and (k &lt; nrow):
            if (m &gt; -1) and (m &lt; ncol):
              temp.append(data[k,m])
      temp.remove(data[i,j])
      max_value = max(temp)
      min_value = min(temp)
      if data[i,j] &gt; max_value:
        new_image[i,j] = max_value
      elif data[i,j] &lt; min_value:
        new_image[i,j] = min_value
        temp =[]
    return new_image.copy()
    
   new_image = aman_effect(image2,5)
plt.figure(figsize=(11,6))
plt.subplot(121), plt.imshow(image2, cmap='gray'),plt.title('Original')
plt.xticks([]), plt.yticks([])
plt.subplot(122), plt.imshow(new_image, cmap='gray'),plt.title('Image Filteration')
plt.xticks([]), plt.yticks([])
plt.show()
