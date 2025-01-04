class Solution {
    public int countTriplets(int[] a, int target) {
        // Code Here
        int n = a.length;
        int count = 0;
        HashMap<Integer, Integer> map = new HashMap<>();
        for(int i=0; i<n; i++){
            for(int j=i+1; j<n; j++){
                int sum = target- (a[i] + a[j]);
                count += map.getOrDefault(sum,0); 
            }
            map.put(a[i],map.getOrDefault(a[i],0)+1);
        }
        return count;
    }
}
