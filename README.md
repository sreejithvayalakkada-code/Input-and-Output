Here is the link to my flowchart:
https://app.diagrams.net/#G1PqHRy4fndFC8oBPWTW-NHEqBQ3cH-bkI#%7B%22pageId%22%3A%22N0QXlHSIybLNl2KS-1lm%22%7D
Here is the link to my code:
https://onecompiler.com/java/43x5vvezn 
Here is a link to my video:
https://screenpal.com/content/video/cTQqh1nDV36?top-banner=online-recorder-details
The actuall code:
import java.util.Scanner;

public class FileNameConverter {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        System.out.println("Enter the list of filenames (each on a new line):");

        // Read the entire input as a single string, assuming multiple lines are pasted
        // or entered until an empty line is provided to signify the end of input.
        StringBuilder inputBuilder = new StringBuilder();
        while (scanner.hasNextLine()) {
            String line = scanner.nextLine();
            if (line.isEmpty()) {
                break; // Stop reading if an empty line is entered
            }
            inputBuilder.append(line).append("\n");
        }
        String input = inputBuilder.toString().trim(); // Trim to remove trailing newline

        // Split the input string into individual filenames
        String[] fileNames = input.split("\n");

        System.out.println("\nConverted filenames:");
        for (String fileName : fileNames) {
            // Replace ".jpg" with "_info.txt"
            String convertedFileName = fileName.replace(".jpg", "_info.txt");
            System.out.println(convertedFileName);
        }

        scanner.close();
    }
}
