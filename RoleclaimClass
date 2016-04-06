public class Roleclaim
{
    private String role;
    private String[] will;

    public Roleclaim()
    {
        role = "";
        will = new String[18];
    }

    public void claimRole(String role, Players arrayListOfPlayers, int nights)
    {
        this.role = role;
        this.will = getWillFormatt(role, arrayListOfPlayers, nights);
    }

    public String[] getWillFormatt(String roleclaim, Players arrayListOfPlayers, int nights)
    {
        String role = roleclaim.toUpperCase();
        if(role.equals("VETERAN"))
            return getVeteranWill(arrayListOfPlayers, nights);
        else if(role.equals("VIGILANTE"))
            return getVigilanteWill(arrayListOfPlayers, nights);
        else if(role.equals("LOOKOUT"))
            return getLookoutWill(arrayListOfPlayers, nights);
        else if(role.equals("SHERIFF"))
            return getSheriffWill(arrayListOfPlayers, nights);
        else if(role.equals("INVESTIGATOR"))
            return getInvestigatorWill(arrayListOfPlayers, nights);
        else if(role.equals("BODYGUARD"))
            return getBodyGuardWill(arrayListOfPlayers, nights);
        else if(role.equals("DOCTOR"))
            return getDoctorWill(arrayListOfPlayers, nights);
        else if(role.equals("ESCORT"))
            return getEscortWill(arrayListOfPlayers, nights);
        else if(role.equals("MEDIUM"))
            return getMediumWill(arrayListOfPlayers, nights);
        else if(role.equals("RETRIBUTIONIST"))
            return getRetributionistWill(arrayListOfPlayers, nights);
        else if(role.equals("TRANSPORTER"))
            return getTransporterWill(arrayListOfPlayers, nights);
        else if(role.equals("SURVIVOR"))
            return getSurvivorWill(arrayListOfPlayers, nights);
        else 
            return will;
    }

    public static String[] getVeteranWill(Players arrayListOfPlayers, int nights)
    {
        String[] will = new String[18];
        will[0] = arrayListOfPlayers.getMyName();
        will[1] = "Veteran";
        will[2] = "";
        int numOfAlerts = 0;
        for(int rep = 1; rep <= nights; rep++)
        {
            if(Math.random() < 0.5 && (rep + 3) < 18 && numOfAlerts < 3)
            {
                will[rep + 2] = "N" + rep + ": ALERT";
                numOfAlerts++;
            }
            else if((rep + 3) < 18)
                will[rep + 2] = "N" + rep + ": NO ALERT";
        }
        return will;
    }
    
    public static String[] getInvestigatorWill(Players arrayListOfPlayers, int nights)
    {
        String[] will = new String[18];
        will[0] = arrayListOfPlayers.getMyName();
        will[1] = "Investigator";
        will[2] = "";
        int numOfAlerts = 0;
        for(int rep = 1; rep <= nights; rep++)
        {
            will[rep + 2] = "N" + rep + ": " + arrayListOfPlayers.getRandomAlivePlayer() + " — " + getInvestResults();
        }
        return will;
    }
    
    public static String getInvestResults()
    {
        int randomNumber = (int) (Math.random()*100);
        String results = "";
        if(randomNumber <= 35)
            results = "BG, Jailor, Lookout";
        else if(randomNumber <= 55 && randomNumber > 35)
            results = "Sheriff, Ret, Exe";
        else if(randomNumber <= 70 && randomNumber > 55)
            results = "Vig, Vet, Maf";
        else if(randomNumber <= 90 && randomNumber > 70)
            results = "Esc, Cons";
        else
            results = "Doc, SK, Vamp";
        return results;
    }
    
    public static String[] getTransporterWill(Players arrayListOfPlayers, int nights)
    {
        String[] will = new String[18];
        will[0] = arrayListOfPlayers.getMyName();
        will[1] = "Transporter";
        will[2] = "";
        int numOfAlerts = 0;
        for(int rep = 1; rep <= nights; rep++)
        {
            will[rep + 2] = "N" + rep + ": " + arrayListOfPlayers.getRandomAlivePlayer() + " <—> " + arrayListOfPlayers.getRandomAlivePlayer();
        }
        return will;
    }
    
    public static String[] getVigilanteWill(Players arrayListOfPlayers, int nights)
    {
        String[] will = new String[18];
        will[0] = arrayListOfPlayers.getMyName();
        will[1] = "Vigilante";
        will[2] = "";
        for(int rep = 1; rep <= nights; rep++)
        {
            if(Math.random() < 0.3 && (rep + 3) < 18)
                will[rep + 2] = "N" + rep + ": Shooting " + arrayListOfPlayers.getRandomAlivePlayer() + " – immune";
            else if((rep + 3) < 18) 
                will[rep + 2] = "N" + rep + ": Not shooting";
        }
        return will;
    }
    
    public static String[] getLookoutWill(Players arrayListOfPlayers, int nights)
    {
        String[] will = new String[18];
        will[0] = arrayListOfPlayers.getMyName();
        will[1] = "Lookout";
        will[2] = "";
        for(int rep = 1; rep <= nights; rep++)
        {
            will[rep + 2] = "N" + rep + ": " + arrayListOfPlayers.getRandomAlivePlayer() + " – NV";
        }
        return will;
    }
    
    public static String[] getSheriffWill(Players arrayListOfPlayers, int nights)
    {
        String[] will = new String[18];
        will[0] = arrayListOfPlayers.getMyName();
        will[1] = "Sheriff";
        will[2] = "";
        for(int rep = 1; rep <= nights; rep++)
        {
            if((rep + 3) < 18)
                will[rep + 2] = "N" + rep + ": " + arrayListOfPlayers.getRandomAlivePlayer() + " – NS";
        }
        return will;
    }
    
    public static String[] getBodyGuardWill(Players arrayListOfPlayers, int nights)
    {
        String[] will = new String[18];
        will[0] = arrayListOfPlayers.getMyName();
        will[1] = "BodyGuard";
        will[2] = "";
        for(int rep = 1; rep <= nights; rep++)
        {
            if((rep + 3) < 18)
                will[rep + 2] = "N" + rep + ": " + arrayListOfPlayers.getRandomAlivePlayer();
        }
        return will;
    }
    
    public static String[] getDoctorWill(Players arrayListOfPlayers, int nights)
    {
        String[] will = new String[18];
        will[0] = arrayListOfPlayers.getMyName();
        will[1] = "Doctor";
        will[2] = "";
        for(int rep = 1; rep <= nights; rep++)
        {
            if((rep + 3) < 18)
                will[rep + 2] = "N" + rep + ": " + arrayListOfPlayers.getRandomAlivePlayer();
        }
        return will;
    }
    
    public static String[] getEscortWill(Players arrayListOfPlayers, int nights)
    {
        String[] will = new String[18];
        will[0] = arrayListOfPlayers.getMyName();
        will[1] = "Escort";
        will[2] = "";
        for(int rep = 1; rep <= nights; rep++)
        {
            if((rep + 3) < 18)
                will[rep + 2] = "N" + rep + ": " + arrayListOfPlayers.getRandomAlivePlayer();
        }        
        if((nights + 5 < 18))
        {
            will[nights + 4] = "";
            will[nights + 5] = "If I am killed by SK, check last roleblocked.";
        }        
        return will;
    }
    
    public static String[] getMediumWill(Players arrayListOfPlayers, int nights)
    {
        String[] will = new String[18];
        will[0] = arrayListOfPlayers.getMyName();
        will[1] = "Medium";
        will[2] = "";
        will[3] = "N1: The curse is not real.";
        for(int rep = 2; rep <= nights; rep++)
        {
            if((rep + 3) < 18 && rep == 3)
                will[rep + 2] = "N3: " + arrayListOfPlayers.getRandomDeadPlayer() + " is salty.";
            else if((rep + 3) < 18 && rep == 4)
                will[rep + 2] = "N4: " + arrayListOfPlayers.getRandomDeadPlayer() + " is annoying.";
            else if((rep + 3) < 18)
                will[rep + 2] = "N" + rep + ": " + "Still no info.";
        }
        return will;
    }
    
    public static String[] getRetributionistWill(Players arrayListOfPlayers, int nights)
    {
        String[] will = new String[18];
        will[0] = arrayListOfPlayers.getMyName();
        will[1] = "Retributionist";
        will[2] = "";
        will[3] = "N1: At least I have a chance to revive.";
        for(int rep = 2; rep <= nights; rep++)
        {
            if((rep + 3) < 18)
                will[rep + 2] = "N" + rep + ": ";
        }
        return will;
    }
    
    public static String[] getSurvivorWill(Players arrayListOfPlayers, int nights)
    {
        String[] will = new String[18];
        will[0] = arrayListOfPlayers.getMyName();
        will[1] = "Survivor";
        will[2] = "";
        int numOfVests = 0;
        for(int rep = 1; rep <= nights; rep++)
        {
            if(Math.random() < 0.5 && (rep + 3) < 18 && numOfVests < 4)
            {
                will[rep + 2] = "N" + rep + ": Used bulletproof vest.";
                numOfVests++;
            }
            else if((rep + 3) < 18)
                will[rep + 2] = "N" + rep + ": No vest used.";
        }
        return will;
    }
    
    public String getRoleclaim()
    {
        return this.role;
    }
    
    public String[] getWill()
    {
        return this.will;
    }
}
