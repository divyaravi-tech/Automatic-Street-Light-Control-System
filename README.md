# Automatic-Street-Light-Control-System
This project simulates an embedded system that automatically turns street light ON at night and OFF during the day using LDR. It helps to save energy and reduce manual control.
#include <stdio.h>

int main() {
    int lightIntensity; // Simulating LDR sensor value (0-100)
    
    printf("---- AUTOMATIC STREET LIGHT CONTROL SYSTEM ----\n");
    printf("Enter surrounding light intensity (0 = dark, 100 = bright daylight): ");
    scanf("%d", &lightIntensity);

    if (lightIntensity < 30) {
        printf("\n🌙 It's Dark Outside.\n");
        printf("Street Lights: ON 💡\n");
    } 
    else if (lightIntensity >= 30 && lightIntensity <= 60) {
        printf("\n🌆 Evening or Cloudy Weather.\n");
        printf("Street Lights: Dim Mode (Energy Saving)\n");
    } 
    else {
        printf("\n☀️ Bright Daylight.\n");
        printf("Street Lights: OFF 🚫\n");
    }

    printf("\nSystem Monitoring Complete.\n");
    return 0;
}
