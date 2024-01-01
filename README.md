1) To get all unseal key run following command
     --------------------------------------------------------------
     | "kubectl exec -ti vault-0 -n vault -- vault operator init" |
     --------------------------------------------------------------

2) Unseal vault using following commands three times with Key 1, Key 2 and Key 3
     ----------------------------------------------------------------
     | "kubectl exec -ti vault-0 -n vault -- vault operator unseal" |
     ----------------------------------------------------------------

3)Lets port forward the vault to localhost
     -----------------------------------------------------
     | "kubectl port-forward vault-0 8200:8200 -n vault" |
     -----------------------------------------------------

4)Now lets login to Vault using vault token and our localhost as we have port-forwarded vault pod to 8200
     --------------------------------------------
     | "export VAULT_ADDR=http://127.0.0.1:8200"|
     |   "vault login <Root_Token>"             |
     --------------------------------------------

5)
