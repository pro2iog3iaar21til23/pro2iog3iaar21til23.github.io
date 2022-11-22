# Her en mulig løsning på problemet i forløb 11...

```java
void setup() {
  int[] usorteret =  {1, 12, 32, 5, 1, 8, 9, 8, 11, 17};
  int[] sorteret  = new int[usorteret.length];

  for (int i=0; i< usorteret.length; i++) {
    int minIndex = 0;
    int minValue = usorteret[minIndex];
    for (int j=0; j< usorteret.length; j++) {
      if (usorteret[j]<minValue) {
        minIndex = j;
        minValue = usorteret[j];
      }
    }
    usorteret[minIndex] = max(usorteret);
    sorteret[i]=minValue;
  }
  printList(usorteret);
  printList(sorteret);
}  

void printList(int[] list) {
  for (int e : list) print(e + " ");
  println();
}

```
