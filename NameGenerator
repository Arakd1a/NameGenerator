
package namegenerator;

import java.io.File;
import java.io.FileNotFoundException;
import java.util.ArrayList;
import java.util.Scanner;

public class NameGenerator {

    
    public static void main(String[] args) {
          
        Scanner inFileNouns = null;
        Scanner inFileVerbs = null;
        Scanner inFilePrepositions = null;
        
        String wordToken;
        
        int nounsArraySize = 0;
        int verbsArraySize = 0;
        int prepositionsArraySize = 0;
        
        int randomNounNumber = 0;
        int randomVerbNumber = 0;
        int randomPrepositionNumber = 0;
        
        String name;
        
        String noun;
        String verb;
        String preposition;
        
         try {
        inFileNouns = new Scanner(new File("./res/nouns.txt")).useDelimiter(",\\s*");
             } catch (FileNotFoundException ex) {
           System.err.println("NOUNS NOT FOUND");
         }
         
          try {
        inFileVerbs = new Scanner(new File("./res/verbs.txt")).useDelimiter(",\\s*");
             } catch (FileNotFoundException ex) {
           System.err.println("VERBS NOT FOUND");
         }
          
           try {
        inFilePrepositions = new Scanner(new File("./res/prepositions.txt")).useDelimiter(",\\s*");
             } catch (FileNotFoundException ex) {
           System.err.println("PREPOSITIONS NOT FOUND");
         }
    
        
        ArrayList<String> nounsArray = new ArrayList<String>();
        while (inFileNouns.hasNextLine()) {
            wordToken = inFileNouns.nextLine();
            nounsArray.add(wordToken);
            nounsArraySize++;
         }
         inFileNouns.close();
         
        ArrayList<String> verbsArray = new ArrayList<String>();
        while (inFileVerbs.hasNextLine()) {
            wordToken = inFileVerbs.nextLine();
            verbsArray.add(wordToken);
            verbsArraySize++;
         }
         inFileVerbs.close();
         
        ArrayList<String> prepositionsArray = new ArrayList<String>();
        while (inFilePrepositions.hasNextLine()) {
            wordToken = inFilePrepositions.nextLine();
            prepositionsArray.add(wordToken);
            prepositionsArraySize++;
         }
         inFilePrepositions.close();
         
         
         
    
            randomNounNumber = (int )(Math.random() * nounsArraySize);
            randomVerbNumber = (int )(Math.random() * verbsArraySize);
            randomPrepositionNumber = (int )(Math.random() * prepositionsArraySize);

            noun = nounsArray.get(randomNounNumber);
            verb = verbsArray.get(randomVerbNumber)+ "s";
            preposition = prepositionsArray.get(randomPrepositionNumber);

            name = verb + " " + preposition + " " + noun;

            System.out.println(name);
         
       
    }
 
}
