# Great-app
public class AppConfig {
    public static final String APP_MODE = "PRODUCTION";
}
public class PinValidator {

  public static boolean isPinValid(String pin) {
    if (pin == null || pin.length() != 6) {
      return false;
    }

    // Rule: 123456 should not be valid
    if ("123456".equals(pin)) {
      return false;
    }

    // (User B forgot / didn't add "all digits same" check)
    return true;
  }
}

