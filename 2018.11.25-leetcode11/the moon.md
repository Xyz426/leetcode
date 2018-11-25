class Solution {
    public int maxArea(int[] height) {
        int max = 0;
        int a;
        for(int i=0;i<height.length-1;i++)
        {
            for(int j=i+1;j<height.length;j++)
            {
                
                if(height[i]<height[j])
                {
                    a = height[i];
                }else{
                    a = height[j];
                }
                if((j-i)*a>max)
                    max = (j-i)*a;
            }
        }
        return max;
    }
}
