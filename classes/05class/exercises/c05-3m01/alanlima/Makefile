RUNNER ?= docker-compose run --rm awscli
BUCKET_NAME?=

create_bucket:
	@$(RUNNER) make _create_bucket
.PHONY:create_bucket

delete_bucket:
	@$(RUNNER) make _delete_bucket
.PHONY:delete_bucket

list_bucket_objects:
	@$(RUNNER) make _list_bucket_objects
.PHONY:list_bucket_objects

_create_bucket:
	@scripts/create_bucket.sh
.PHONY:_create_bucket

_delete_bucket:
	@scripts/delete_bucket.sh
.PHONY:_delete_bucket

_list_bucket_objects:
	@echo "š¤: You again, I cannot even enjoy my standby moments in peace."
	@echo "š¤: So now you want me to give you a list of the objects?"
	@echo "š¤: Such a lazy human, just go to the aws console š. Fine here is the list:" 
	@aws s3 ls --human-readable --summarize s3://${BUCKET_NAME}
	@echo -e "\nš¤: anything else? maybe a mojito cocktail šø?"
.PHONY:_list_bucket_objects