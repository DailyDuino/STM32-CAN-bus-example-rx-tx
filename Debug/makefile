################################################################################
# Automatically-generated file. Do not edit!
################################################################################

-include ../makefile.init

RM := rm -rf

# All of the sources participating in the build are defined here
-include sources.mk
-include Drivers/STM32F1xx_HAL_Driver/Src/subdir.mk
-include Core/Startup/subdir.mk
-include Core/Src/subdir.mk
-include subdir.mk
-include objects.mk

ifneq ($(MAKECMDGOALS),clean)
ifneq ($(strip $(C_DEPS)),)
-include $(C_DEPS)
endif
endif

-include ../makefile.defs

# Add inputs and outputs from these tool invocations to the build variables 
EXECUTABLES += \
CAN_Rx_Tx_Example.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
CAN_Rx_Tx_Example.list \

OBJCOPY_BIN += \
CAN_Rx_Tx_Example.bin \


# All Target
all: CAN_Rx_Tx_Example.elf secondary-outputs

# Tool invocations
CAN_Rx_Tx_Example.elf: $(OBJS) $(USER_OBJS) C:\Users\cyril\STM32CubeIDE\workspace_1.0.2\CAN_Rx_Tx_Example\STM32F103C8TX_FLASH.ld
	arm-none-eabi-gcc -o "CAN_Rx_Tx_Example.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"C:\Users\cyril\STM32CubeIDE\workspace_1.0.2\CAN_Rx_Tx_Example\STM32F103C8TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="CAN_Rx_Tx_Example.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

CAN_Rx_Tx_Example.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "CAN_Rx_Tx_Example.list"
	@echo 'Finished building: $@'
	@echo ' '

CAN_Rx_Tx_Example.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "CAN_Rx_Tx_Example.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
