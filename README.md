public class Chall3 {
  public static String decrypt(String text) {
    StringBuilder decryptedText = new StringBuilder();
    for (int i = 0; i < text.length(); i++) {
      char c = text.charAt(i);
      if (Character.isLetter(c)) {
        char base = Character.isLowerCase(c) ? 'a' : 'A';
        decryptedText.append((char)((c - base + 13) % 26 + base));
      } else {
        decryptedText.append(c);
      } 
    } 
    return decryptedText.toString();
  }
  
  public static void main(String[] args) {
    String originalText = "RUP{wq_th1_s0e_w4i4_q3ohtt3e}";
    String decryptedText = decrypt(originalText);
    System.out.println ("flag is :"+decryptedText);
  }
}

<!---
Dcoco22/Dcoco22 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
