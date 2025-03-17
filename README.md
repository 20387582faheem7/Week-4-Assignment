# Week-4-Assignment
       # Ask user for filename
      filename = input("Enter the name of the file to read: ")

      # Open the file for reading
        with open(filename, "r") as file:
            content = file.readlines()  # Read file as a list of lines

        # Modify the content (Example: Convert text to uppercase)
        modified_content = [line.upper() for line in content]

        # Write the modified content to a new file
        new_filename = "modified_" + filename
        with open(new_filename, "w") as new_file:
            new_file.writelines(modified_content)

        print(f"Modified content has been saved to {new_filename}")

    except FileNotFoundError:
        print("Error: The file does not exist. Please check the filename and try again.")

    except PermissionError:
        print("Error: You don't have permission to access this file.")

    except Exception as e:
        print(f"An unexpected error occurred: {e}")


