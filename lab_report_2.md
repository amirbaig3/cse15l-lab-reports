# Lab Report 2 - Servers and SSH Keys


`
public String handleRequest(URI url) {
    if (url.getPath().equals("/")) {
        return str;
    } else {
        if (url.getPath().contains("/add-message")) {
            String[] parameters = url.getQuery().split("=");
            if (parameters[0].equals("s")) {
                buildString(parameters[1]);
            }
            return str;
        }
        return "404 Not Found!";
    }
}

private void buildString(String inputString){
    if (len == 0) {
        str = "1. " + inputString + "\n";
        len++;
    } else {
        str = str + String.valueOf(len + 1) + ". " + inputString + "\n";
        len++;
    }
}
`

## Part 1
![1](images/lab-2/StringServer-1.png)
- 
-
-
-

![2](images/lab-2/StringServer-2.png)
-
-
-
-
