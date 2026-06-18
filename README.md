# Great-app
public class AppConfig {
    public static final String APP_MODE = "Staging";
}
public class PinValidator {

  public static boolean isPinValid(String pin) {
    if (pin == null || pin.length() != 6) {
      return false;
    }

    // Invalid if all digits are the same (000000 .. 999999)
    char first = pin.charAt(0);
    for (int i = 1; i < pin.length(); i++) {
      if (pin.charAt(i) != first) {
        return true; // Not all digits are the same => valid
      }
    }

    return false; // All digits matched the first digit => invalid
  }
}
