# Login to your Azure Subscription
#az login 

# Declare variables
resourceGroupName='LINUX-RG'
vmName='ubuntu01'

# Get VM OS disk name
vmdiskname=$(az vm show --resource-group $resourceGroupName --name $vmName -d --query "storageProfile.osDisk.name" -o tsv)

# Get VM OS disk create date
createDate=$(az disk show --resource-group LINUX-RG --name $vmdiskname --query "timeCreated" -o tsv)

# Convert the date to readable format
createDatef=$(date -d $createDate '+%Y/%m/%d %T')

# Output
printf "%-20s | %-20s | %-20s\n" "$resourceGroupName" "$vmName" "$createDatef"