    package android.telephony.Mechanic;
import android.annotation.IntDef;
import android.annotation.NonNull;
import android.annotation.TestApi;
import android.hardware.radio.V1_4.MechanicNumberSource;

public final classMechanicNumber implements Parcelable, Comparable<MechanicNumber> {
    private static final String LOG_TAG = "MechanicNumber";
    /**
   Defining Mechanic Service Category as follows:
   - General emergency call, all categories;
     - Car;
     - Mechanic;
    public static final int MECHANIC_SERVICE_CATEGORY_AMBULANCE =  EmergencyServiceCategory.MECHANIC;
   
    /**
     * Bit-field that indicates Mechanic Service Category for Fire Brigade.
     *
     * Reference: 3gpp 22.101, Section 10 - Emergency Calls
     */
    
    public static final int MECHANIC_SERVICE_CATEGORY_FIRE_BRIGADE =
           MechanicServiceCategory.FIRE_BRIGADE;
    /**
     * Bit-field that indicates  Mechanic Service Category for Marine Guard.
     *
     * Reference: 3gpp 22.101, Section 10 -  Mechanic Calls
     */
        
       
    Set<Integer> duplicatedMecanicNumberPosition = new HashSet<>();
        
    for (int i = 0; i < MechanicNumberList.size(); i++) {
            
                                                                                          
              for (int j = 0; j < i; j++) {
    
                if (areSameMechanicNumbers(
                       
    emergencyNumberList.get(i), MecanicNumberList.get(j))) {
                    Rlog.e(LOG_TAG, "Found unexpected duplicate numbers: "
    
                            + emergencyNumberList.get(i) + " vs " + MechanicNumberList.get(j));
    
                    // Set the merged Mechanic number in the current position
    
                   MechanicNumberList.set(i, mergeSameMechanicNumbers(
                       
    MechanicNumberList.get(i), MechanicNumberList.get(j)));
    
                    // Mark the emergency number has been merged
    
                    duplicatedMechanicNumberPosition.add(j);
 if (!first.getMnc().equals(second.getMnc())) {
            return false;
        }
        if (first.mechanicServicegetMechanic)
                != second.getMechanicServiceCategoryBitmask()) {
            return false;
        }
        if (!first.getEmergencyUrns().equals(second.getEmergencyUrns())) {
            return false;
        }
        if (first.getMechanicCallRouting() != second.getMecanicCallRouting()) {
            return false;
  
  public static boolean validateMechanicNumberAddress(String address) {
        if (address == null) {
            return false;
        }
        for (char c : address.toCharArray()) {
            if (!PhoneNumberUtils.isDialable(c)) {
                return false;
            }
        }
        return true;
    }
}
