public class binary_search {
    public static void main(String[] args) {
        int arr[] = {1,2,4,5,7,9,11,13,15,19,20,22,24,28,31,36,39,45,47,50,54,58,59,60,64,67,68,71,74,77,79,84,86,88,91,93,97,99,100};
        int n=arr.length,index = -1,e = n - 1, cnt=0;
        int s = 0, key=99;

        while (s<=e) {
            int m=s+(e-s)/2;
            if (arr[m] == key) {
                cnt++;
                index = m;
                break;
            }
            else if (arr[m] < key) {
                s = m + 1;
            }
            else {
                e = m - 1;
            }
        }

        if (cnt>0) {
            System.out.println("Element cnt at index: " + index);
        } else {
            System.out.println("Element not cnt.");
        }
    }
}