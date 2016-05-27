// run only on slave-terry node 
node ('slave-terry') {
   stage 'Stage 1'
   echo 'Hello World 1 pikachu!!v'
   stage 'Stage 2'
   // display the docker version
   def dockerVer = captureOutput('docker -v')
   echo "$dockerVer";
   // display the node version
   def nodeVer = captureOutput('node -v')
   echo "Node Ver=$nodeVer";
}
def captureOutput(String cmd) {
   sh "${cmd} > result";
   def output=readFile('result').trim()
   output;
}
