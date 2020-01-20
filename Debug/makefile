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
Blink\ without\ Delay.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Blink\ without\ Delay.list \

OBJCOPY_HEX += \
Blink\ without\ Delay.hex \


# All Target
all: Blink\ without\ Delay.elf secondary-outputs

# Tool invocations
Blink\ without\ Delay.elf: $(OBJS) $(USER_OBJS) E:\Karedox.com\Firmware\Blink\ without\ Delay\STM32F103C6TX_FLASH.ld
	arm-none-eabi-gcc -o "Blink without Delay.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"E:\Karedox.com\Firmware\Blink without Delay\STM32F103C6TX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Blink without Delay.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Blink\ without\ Delay.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Blink without Delay.list"
	@echo 'Finished building: $@'
	@echo ' '

Blink\ without\ Delay.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "Blink without Delay.hex"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
