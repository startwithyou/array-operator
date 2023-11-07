# array-operator
<!DOCTYPE html>
<html lang="en">
  <head>
    <title>Array Operations</title>
  </head>
  <body>
    <h1>Javascript Practical of Array manipulation</h1>

    <script>
      var array = [];
      var x = prompt("Enter the size of array");
      //Input the elements in the array
      for (i = 0; i < x; i++) {
        array[i] = prompt("Enter array Element " + (i + 1));
      }
      //Display the array elements
      document.write("Array entered is" + "</br> </br>");
      for (i = 0; i < x; i++) {
        document.write(
          "The element at position " + i + " is : " + array[i] + "</br> </br>"
        );
      }

      //A. Remove element from array

      function removeElement(removeEle) {
        var removeEle = prompt("Enter array Element to delete ");
        for (i = 0; i < x; i++) {
          if (array[i] == removeEle) {
            // array.remove(i);
            document.write(
              "After deleting array element:  " +
                array[i] +
                "   array is" +
                "</br> </br>"
            );
            delete array[i];
          }
        }
      }

      //B. Check for a specific value

      function searchElement(searchEle) {
        var searchEle = prompt("Enter array Element to find ");
        let pres = false;
        pres = array.includes(searchEle);
        if (pres == true) {
          document.write(
            "Element " + searchEle + " is present in the array</br></br>"
          );
        } else
          document.write(
            "Element " + searchEle + "  is not present in the array</br></br>"
          );
      }
      //searchElement(searchEle);

      //C. To empty an array
      function emptyArray() {
        array.splice(0, array.length);
        if (array.length == 0) {
          document.write("Array is empty now using splice method");
        }
        document.write(array);
      }

      removeElement();

      //Display the array elements
      for (i = 0; i < x; i++) {
        document.write(
          "The element at position " + i + " is : " + array[i] + "</br> </br>"
        );
      }

      searchElement();

      emptyArray();
    </script>
  </body>
</html>
