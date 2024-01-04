1. 배열의 오름차순   
    ① Arrays.sort(배열)을 사용하여 배열의 요소들을 오름차순으로 재정리한다. 
    - 예시 : int[] intArr = new int[] {1,3,5,2,4};                          //Primitive Type                          
            double[] doubletArr = new double[] {1.1, 3.3, 5.5, 2.2, 4.4};        //Primitive Type  
            String[] stringArr = new String[] {"A","C","B","E","D"}; //Reference type(Wrapper Class)    
            Arrays.sort(intArr); -> intArr : 1 2 3 4 5           
            Arrays.sort(doubletArr); -> doubletArr : 1.1 2.2 3.3 4.4 5.5   
            Arrays.sort(stringArr); -> stringArr : A B C D E
    - 일부구간만 오름차순 정렬도 가능하다.  
      -> 예시  
      int[] intArr = new int[] {1,3,5,2,4};  
      Arrays.sort(intArr,2,5);  // intArr[2]~intArr[4]의 값 (5,2,4) 만 정렬 (toIndex 이전 index까지)   
      -> intArr : 1 3 2 5 4
2. 배열의 내림차순  
   ① Arrays.sort(배열, Collections.reverseOrder());을 사용하여 배열의 요소들을 내림차순으로 재정리한다.  
   - 예시 : String[] stringArr = new String[] {"A","C","B","E","D"}; //Reference type(Wrapper Class)  
     Arrays.sort(stringArr, Collections.reverseOrder()); -> stringArr : E D C B A  
   - ** Primitive Type의 배열은 위와 같은 방법으로 내림차순이 불가능하므로 반드시 아래와 같이 Wrapper Class로 변환 후 내림차순을 해야한다.  
     -> 예시 : int[] -> Integer[], double[] -> Double[]
     