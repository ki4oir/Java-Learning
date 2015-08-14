/*
 * Survey Class
 * By: Curtis Morris
 * Date: 7/20/15
 */
package surveyit152;

import java.util.Scanner;

public class Survey { //begin Survey object blueprint

    private static int respondentId; //respondent ID variable; holds the integer variable for the respondent ID
    private String surveyTitle; //surveyTitle variable; holds the string for the survey title
    static int numRespondents = 3; //number of respondents as integer
    static int numQuestions = 3; //number of questions as integer
    String questionArray[] = new String[numQuestions]; //array holds questions
    int responseArray[][] = new int [numQuestions][numRespondents]; //2D array to hold answers
    Scanner input = new Scanner(System.in);

    Survey() {
        this("Customer Survey"); 
        //passes the string "Customer Survey" to the method 
        //Survey(String surveyTitle) and returns it here. 
    }

    Survey( String surveyTitle ){
        //this sets the respondentId to zero and selects the survey title
        
        respondentId = 0;
        this.surveyTitle = surveyTitle; //forces the program to use the surveyTitle in this method

    }

    String getSurveyTitle() { //begins the getSurveyTitle method; 
                              //is package private when there isn't an 
                              //access modifier such as "public" in front.
    
        return surveyTitle; //returns the survey Title
    }
    
    int generateRespondentId() {//the generateRespondentId method is also package private
                                //it increments the respondent ID and then returns the respondentId value
                                //the output begins at 1 because it is incremented first.
        
        return ++respondentId; //increments respondentId then returns the respondent ID

    }
    
    void displaySurveyResults() {
        System.out.printf("The title of this survey is %s%n", surveyTitle);
        
        for (int respondent = 0; respondent < numRespondents; respondent++) {
            for (int question = 0; question < numQuestions; question++) {
                System.out.print(responseArray[respondent][question] + "\t");
            }
            System.out.println("");
        }
    }
    
    void logResponse(int respondentId, int questionNum, int response) {
        
        responseArray[respondentId][questionNum] = response;
    }
    
    void displayQuestionStats(int questionNum) {
        System.out.println("Enter a question numer to see results: ");
        questionNum = input.nextInt();
        
        for(int respondent = 0; respondent < numRespondents; respondent++){
        System.out.println(responseArray[respondent][(questionNum-1)]);
        }
        
    }
    
    void enterQuestions(){
        System.out.println("Please enter the survey Questions");
        for(int counter = 0; counter < numQuestions; counter++){
            System.out.println("Please enter question " + counter);
            String questionIn = input.next();
            questionArray[counter] = questionIn;
        }
        for(int countera = 0; countera < numQuestions; countera++){
            System.out.printf("%5s%8s%n", countera, questionArray[countera]);
        }
    }
}
