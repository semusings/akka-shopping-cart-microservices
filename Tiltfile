local_resource(name='k8s-apply', cmd='task deploy', labels=["k8s"], auto_init=False, trigger_mode=TRIGGER_MODE_MANUAL)
local_resource(name='k8s-destroy', cmd='task destroy', labels=["k8s"], auto_init=False, trigger_mode=TRIGGER_MODE_MANUAL)

local_resource(name='order-build', cmd='task order-service:k8s-build', labels=["build"], allow_parallel=True, auto_init=False, trigger_mode=TRIGGER_MODE_MANUAL)
local_resource(name='cart-build', cmd='task cart-service:k8s-build', labels=["build"], allow_parallel=True, auto_init=False, trigger_mode=TRIGGER_MODE_MANUAL)
local_resource(name='analytics-build', cmd='task analytics-service:k8s-build', labels=["build"], allow_parallel=True, auto_init=False, trigger_mode=TRIGGER_MODE_MANUAL)
