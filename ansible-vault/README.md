# Ansible Vault

## ansible-vault command

encryption/decryption utility for Ansible data files positional arguments:

```
  {create,decrypt,edit,view,encrypt,encrypt_string,rekey}

    create              Create new vault encrypted file
    decrypt             Decrypt vault encrypted file
    edit                Edit vault encrypted file
    view                View vault encrypted file
    encrypt             Encrypt YAML file
    encrypt_string      Encrypt a string
    rekey               Re-key a vault encrypted file
```


### Create new file with ansible-vault

```bash
ansible-vault create ArquivoCriadoPeloVault
```

### View file with ansible-vault

```bash
ansible-vault view ArquivoCriadoPeloVault
```

### Edit file with ansible-vault

```bash
ansible-vault edit ArquivoCriadoPeloVault
```

### Encrypt file exists with ansible-vault

```bash
ansible-vault encrypt ArquivoExistenteEncriptadoComVault
```

### Encrypt the new file of out the file exists with ansible-vault

```bash
ansible-vault encrypt ArquivoNaoEncriptadoComVault --output=ArquivoNaoEncriptadoComVaultAgoraSim
```

### Decrypt file with ansible-vault

```bash
ansible-vault decrypt ArquivoNaoEncriptadoComVaultAgoraSim
```

## Using vault with playbooks

```bash
ansible-playbook --ask-vault-pass arquivo_encrypt
```
