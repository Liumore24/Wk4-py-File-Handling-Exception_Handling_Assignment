# Wk4-py-File-Handling-Exception_Handling_Assignment

# Function to read from a file and write to a new file with modifications
def process_file(input_filename, output_filename):
    try:
        # Open and read the input file
        with open(input_filename, 'r') as infile:
            content = infile.read()

        # Modify the content (convert to uppercase)
        modified_content = content.upper()

        # Write the modified content to the output file
        with open(output_filename, 'w') as outfile:
            outfile.write(modified_content)
        
        print(f"File processed successfully! The modified content is saved to {output_filename}.")
    
    except FileNotFoundError:
        print(f"Error: The file '{input_filename}' does not exist.")
    except IOError:
        print("Error: There was an issue reading or writing the file.")

# Example usage
input_filename = 'input.txt'  # Replace with your input file name
output_filename = 'output.txt'  # Replace with your desired output file name
process_file(input_filename, output_filename)
