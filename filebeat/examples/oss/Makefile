default: test

include ../../../helpers/examples.mk

RELEASE := helm-filebeat-oss

install:
	helm upgrade --wait --timeout=900 --install $(RELEASE) --values values.yaml ../../

test: install goss

purge:
	helm del --purge $(RELEASE)
