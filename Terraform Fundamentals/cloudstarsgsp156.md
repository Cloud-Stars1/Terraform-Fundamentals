# Terraform Fundamentals || GSP156

### Run the following Commands in the Cloud shell


```
export ZONE=
```




```
gcloud auth list 

cat > instance.tf <<EOF_END
resource "google_compute_instance" "terraform" {
  project      = "$DEVSHELL_PROJECT_ID"
  name         = "terraform"
  machine_type = "e2-medium"
  zone         = "$ZONE"

  boot_disk {
    initialize_params {
      image = "debian-cloud/debian-11"
    }
  }

  network_interface {
    network = "default"
    access_config {
    }
  }
}
EOF_END

terraform init
terraform plan
terraform apply --auto-approve
```

### Congratulations 🎉 for completing the Lab !

##### You Have Successfully Demonstrated Your Skills And Determination.

#### *Well done!*

#### Don't Forget to Join the [Telegram Channel](https://t.me/cloudstars24)

### Subscribe to our YouTube Channel [CLOUD STARS](https://www.youtube.com/@cloud-stars)
