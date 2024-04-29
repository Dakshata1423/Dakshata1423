from PIL import Image

def compress_image(input_image_path, output_image_path):
    # Open the input image
    input_image = Image.open(input_image_path)
    
    # Save the image in a lossless format (PNG)
    input_image.save(output_image_path, format='PNG')
    
    # Close the image
    input_image.close()

if __name__ == "__main__":
    input_image_path = input("Enter the path to the input image: ")
    output_image_path = input("Enter the path where you want to save the compressed image: ")

    # Compress the image
    compress_image(input_image_path, output_image_path)
    print("Compression applied successfully!")
