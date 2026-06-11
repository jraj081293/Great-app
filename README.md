# Great-app
public class AppConfig {
    public static final String APP_MODE = "PRODUCTION";
}
public class PinValidator {

  public static boolean isPinValid(String pin) {
    // Rule: not valid if all digits are the same
    boolean allSame = true;
    for (int i = 1; i < pin.length(); i++) {
      if (pin.charAt(i) != pin.charAt(0)) {
        allSame = false;
        break;
      }
    }
    if (allSame) {
      return false;
    }

    // (User A forgot / didn't add 123456 check)
    return pin != null && pin.length() == 6;
  }
}



