import java.util.ArrayList;
public class Players
{
    private ArrayList<String> alive;
    private ArrayList<String> dead;
    private String myName;

    /**
     * Constructor for objects of class Players
     */
    public Players()
    {
        this.alive = new ArrayList<String>();
        this.dead = new ArrayList<String>();
        this.myName = "";
    }

    public void setMyName(String str)
    {
        this.myName = str;
    }

    public void addPlayer(String str)
    {
        this.alive.add(str);
    }

    public void swapPlayer(String str, String swap)
    {
        if(swap.equals("KILLED"))
        {
            for(int rep = this.alive.size() -1; rep >= 0; rep--)
            {
                if(this.alive.get(rep).equals(str))
                {
                    this.alive.remove(rep);
                    this.dead.add(str);
                }
            }
        }
        else
        {
            for(int rep = this.dead.size() -1; rep >= 0; rep--)
            {
                if(this.dead.get(rep).equals(str))
                {
                    this.dead.remove(rep);
                    this.alive.add(str);
                }
            }
        }
    }

    public String getRandomAlivePlayer()
    {
        int position = (int) (Math.random()*alive.size());
        return alive.get(position);
    }

    public String getRandomDeadPlayer()
    {
        int position = (int) (Math.random()*dead.size());
        return dead.get(position);
    }

    public ArrayList<String> getAlive()
    {
        return this.alive;
    }

    public ArrayList<String> getDead()
    {
        return this.dead;
    }

    public String getMyName()
    {
        return this.myName;
    }
}
