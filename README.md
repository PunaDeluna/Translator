# Translator
Portu - Spain
import com.google.cloud.translate.*;

public class SpanishToPortugueseTranslator {
  public static void main(String[] args) {
    // Instantiates a client
    Translate translate = TranslateOptions.getDefaultInstance().getService();

    // The text to translate
    String text = "Hola, ¿cómo estás?";

    // Translates the text into Portuguese
    Translation translation = translate.translate(text, TranslateOption.sourceLanguage("es"), TranslateOption.targetLanguage("pt"));

    // Prints the translation
    System.out.printf("Texto original: %s%n", text);
    System.out.printf("Traducción: %s%n", translation.getTranslatedText());
  }
}
