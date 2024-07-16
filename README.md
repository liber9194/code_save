# code_save
class Solution {
    public int solution(String my_string) {
        int answer = 0;
        String num1 = "";
        String num2 = "";
        String cost = "";
        int index = 0;
        
        for(int i = 0; i < my_string.length(); ++i)
        {
            if(my_string.charAt(i) == '+' || my_string.charAt(i) == '-')
            {
                cost += my_string.charAt(i);
                index = i;
            }
        }
        
        for(int i = 0; i < index; ++i)
        {
            if(my_string.charAt(i) != ' ')
            {
                num1 += my_string.charAt(i);
            }
        }
        
        for(int i = index+1; i < my_string.length(); ++i)
        {
            if(my_string.charAt(i) != ' ')
            {
                num2 += my_string.charAt(i);
            }
        }
        
        System.out.println(Integer.parseInt(num1) + " " + num2);
        
        if(cost == "+")
        {
            answer = Integer.parseInt(num1) + Integer.parseInt(num2);
        }
        else
        {
            answer = Integer.parseInt(num1) - Integer.parseInt(num2);
        }
        return answer;
    }
}
