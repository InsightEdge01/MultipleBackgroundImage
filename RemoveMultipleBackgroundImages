import os
from rembg import remove
from PIL import Image

#Define input and output folders
input_folder = "input_images"
output_folder = "output_images"

#loop through all the files in the input folder
for filename in os.listdir(input_folder):
    #check if the file is an image file
    if filename.endswith('.jpg') or filename.endswith('.png'):
        #Define input and output file paths
        input_path = os.path.join(input_folder,filename)
        output_path = os.path.join(output_folder,filename.split('.')[0]+'.png')

        #load the input image
        input_image = Image.open(input_path)

        #Remove the background using rembg
        output_image = remove(input_image)

        #save the output image as a PNG file
        output_image.save(output_path)
