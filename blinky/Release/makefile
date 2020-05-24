################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include nRF_SoftDevice/subdir.mk
-include nRF_Segger_RTT/subdir.mk
-include nRF_Log/subdir.mk
-include nRF_Libraries/subdir.mk
-include nRF_Drivers/subdir.mk
-include nRF_BLE_Services/subdir.mk
-include nRF_BLE/subdir.mk
-include Source\ Files/subdir.mk
-include Board\ Support/subdir.mk
-include Board\ Definition/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(ASM_DEPS)),)
-include $(ASM_DEPS)
endif
ifneq ($(strip $(S_UPPER_DEPS)),)
-include $(S_UPPER_DEPS)
endif
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
SECONDARY_FLASH += \
blinky.hex \

SECONDARY_SIZE += \
blinky.siz \


# All Target
all: blinky.elf secondary-outputs

# Tool invocations
blinky.elf: $(OBJS) $(USER_OBJS)
	@echo 'Building target: $@'
	@echo 'Invoking: GNU ARM Cross C Linker'
	arm-none-eabi-gcc -mcpu=cortex-m0 -mthumb -mabi=aapcs -mfloat-abi=soft -fno-strict-aliasing --short-enums -O3 -fmessage-length=0 -fsigned-char -ffunction-sections -fdata-sections -fno-builtin -T "/media/mj/TOSHIBAEXT/eclipse-workspace/blinky/blinkyLinker.ld" -Xlinker --gc-sections -L/opt/nRF5_SDK_12.3.0_d7731ad/components/toolchain/gcc -Wl,-Map,"blinky.map" --specs=nano.specs -o "blinky.elf" $(OBJS) $(USER_OBJS) $(LIBS)
	@echo 'Finished building target: $@'
	@echo ' '

blinky.hex: blinky.elf
	@echo 'Invoking: GNU ARM Cross Create Flash Image'
	arm-none-eabi-objcopy -O ihex "blinky.elf"  "blinky.hex"
	@echo 'Finished building: $@'
	@echo ' '

blinky.siz: blinky.elf
	@echo 'Invoking: GNU ARM Cross Print Size'
	arm-none-eabi-size --format=berkeley "blinky.elf"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) $(OBJS)$(SECONDARY_FLASH)$(SECONDARY_SIZE)$(ASM_DEPS)$(S_UPPER_DEPS)$(C_DEPS) blinky.elf
	-@echo ' '

secondary-outputs: $(SECONDARY_FLASH) $(SECONDARY_SIZE)

.PHONY: all clean dependents

-include ../makefile.targets
