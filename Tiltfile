docker_compose("./etc/docker/compose.infra.yaml")
dc_resource('kafka', labels=["01-infra"], auto_init=False, trigger_mode=TRIGGER_MODE_MANUAL)
dc_resource('db', labels=["01-infra"], auto_init=False, trigger_mode=TRIGGER_MODE_MANUAL)

docker_compose("./etc/docker/compose.cart.yaml")
local_resource(name='cart-build', cmd='task cart-service:docker-build', labels=["cart-service"], allow_parallel=True, auto_init=False, trigger_mode=TRIGGER_MODE_MANUAL)
dc_resource('cart-service1', labels=["cart-service"], resource_deps=['cart-build'], auto_init=False, trigger_mode=TRIGGER_MODE_MANUAL)
dc_resource('cart-service2', labels=["cart-service"], resource_deps=['cart-build'], auto_init=False, trigger_mode=TRIGGER_MODE_MANUAL)
dc_resource('cart-service3', labels=["cart-service"], resource_deps=['cart-build'], auto_init=False, trigger_mode=TRIGGER_MODE_MANUAL)

docker_compose("./etc/docker/compose.order.yaml")
local_resource(name='order-build', cmd='task order-service:docker-build', labels=["order-service"], allow_parallel=True, auto_init=False, trigger_mode=TRIGGER_MODE_MANUAL)
dc_resource('order-service1', labels=["order-service"], resource_deps=['order-build'], auto_init=False, trigger_mode=TRIGGER_MODE_MANUAL)
dc_resource('order-service2', labels=["order-service"], resource_deps=['order-build'], auto_init=False, trigger_mode=TRIGGER_MODE_MANUAL)
dc_resource('order-service3', labels=["order-service"], resource_deps=['order-build'], auto_init=False, trigger_mode=TRIGGER_MODE_MANUAL)

local_resource(name='analytics:build', cmd='task analytics-service:docker-build', labels=["analytics-service"], allow_parallel=True, auto_init=False, trigger_mode=TRIGGER_MODE_MANUAL)