# Spotless Terraform Test

After running

```bash
./gradlew spotlessApply
```

we should see the following diff:

```diff
diff --git a/terraform/main.tf b/terraform/main.tf
index 8d2ea6f..1f0b04a 100644
--- a/terraform/main.tf
+++ b/terraform/main.tf
@@ -1,6 +1,6 @@
 resource "aws_instance" "example" {
   count = 2

-  ami = "abc123"
+  ami           = "abc123"
   instance_type = "t2.micro"
 }
```
