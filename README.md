def read_and_modify_file(input_filename, output_filename):
    try:
        # Try to open and read the input file
        with open(input_filename, 'r') as infile:
            content = infile.read()

        # Modify the content (example modification: convert to uppercase)
        modified_content = content.upper()

        # Write the modified content to the output file
        with open(output_filename, 'w') as outfile:
            outfile.write(modified_content)

        print(f"Modified content has been written to {output_filename}")

    except FileNotFoundError:
        print(f"Error: The file {input_filename} does not exist.")
    except IOError:
        print(f"Error: The file {input_filename} cannot be read.")

if __name__ == "__main__":
    # Prompt the user for the input filename
    input_filename = input("Enter the name of the file to read: ")
    # Define the output filename
    output_filename = "modified_" + input_filename

    # Call the function to read and modify the file
    read_and_modify_file(input_filename, output_filename)
