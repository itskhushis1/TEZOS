# REVA-TEZOS
TEZO-PAY
The script makes use of a 'float' account on a system with a running Tezos node.
### Usage help and command line argument handling.




function usage() {
  echo "Usage instructions:"
  echo "bash tezos-batch-payments.bash [options]"
  echo -e "  -h --help\t\tPrint this help info."
  echo -e "  --fee AMOUNT\tOverride per-transaction fee (default: 1792 µXTZ)."
  echo -e "  --transactions\tTransactions to run. E.g. \`ADDR1=AMOUNT1,ADDR2=AMOUNT2,...\`"
  echo -e "  --transactions-file\tPath to a file with one \`ADDR=AMOUNT\` per line."
  echo -e "  --docker NETWORK\tUse this option if you use are using the docker scripts to run your node."
  echo -e "  --use NAME\t\tSpecify the name (alias) of an account to use."
  echo -e "  --skip-funding\tDon't ask to fund the account (for instance if it's already funded)."
  echo -e "  --check\t\tCheck node access, parse provided transactions and show the total, then exit."
  echo -e "  --debug\t\tWill output a bunch of extra info during processing."
  echo
  echo "* Note: All 'AMOUNT' values must be in µXTZ (multiply XTZ by 1,000,000)"
  echo "        e.g. to send 12.052 XTZ, specify 12052000 as AMOUNT"
  echo
}
