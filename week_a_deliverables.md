# Week A Assignment - Deliverables
----
Show your work:
1) Browser proof
        Open: http://<EXTERNAL_IP>/

![Browser Proof](/screenshots/browser_proof.jpg)

2) at the end of the lesson, SSH into your VM and curl it
    curl localhost
    curl -s localhost | head  
---
![curl localhost](/screenshots/curl_localhost-1.jpg) 

![curl localhost-1](/screenshots/curl_localhoost-2.jpg)  

![curl-s localhost-1](/screenshots/curl-s_localhost_head.jpg)

---
![Systemctl --nopager](/screenshots/systemctl-nopager.jpg)  

## Section #2

1) Machine proof
        curl -s localhost/healthz

![curl -s localhost/healthz](/screenshots/healthz.jpg)  

---

2) Engineer proof 
        curl -s localhost/metadata | jq .  

![curl metadata](/screenshots/curl_metadata.jpg)    

## Section 3 - Gate Checks

1. Run Gate checks - 
    - note in order for gate_gcp_vm_http_ok.sh to run, we need to change permissions on file. 
    `chmod +x gate_gcp_vm_http_ok.sh`
2. Find the <external IP> of your instance and run gate check script as follows:
`VM_IP=34.135.105.5 ./gate_gcp_vm_http_ok.sh`  

3. Output:  
![Gate Check Output](/screenshots/gate_check_output.jpg)

4. Gate check script creates files in current directory:  

![Gate Check output files](/screenshots/gate_check_output_files.jpg)
5. Contents of gate_result.json

`{
  "lab": "SEIR-I Lab 1",
  "target": "34.135.105.5",
  "status": "PASS",
  "details": [
  "PASS: Homepage reachable (HTTP 200)",
  "PASS: /healthz endpoint returned 'ok'",
  "PASS: /metadata returned valid JSON",
  "PASS: metadata contains instance_name",
  "PASS: metadata contains region"
],
  "failures": [
  ""
]
}`





  