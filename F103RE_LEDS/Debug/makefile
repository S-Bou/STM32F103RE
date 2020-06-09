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
F103RE_LEDS.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
F103RE_LEDS.list \

OBJCOPY_HEX += \
F103RE_LEDS.hex \

OBJCOPY_BIN += \
F103RE_LEDS.bin \


# All Target
all: F103RE_LEDS.elf secondary-outputs

# Tool invocations
F103RE_LEDS.elf: $(OBJS) $(USER_OBJS) D:\Projects\STM32F103RE\F103RE_LEDS\STM32F103RETX_FLASH.ld
	arm-none-eabi-gcc -o "F103RE_LEDS.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"D:\Projects\STM32F103RE\F103RE_LEDS\STM32F103RETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="F103RE_LEDS.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

F103RE_LEDS.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "F103RE_LEDS.list"
	@echo 'Finished building: $@'
	@echo ' '

F103RE_LEDS.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "F103RE_LEDS.hex"
	@echo 'Finished building: $@'
	@echo ' '

F103RE_LEDS.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "F103RE_LEDS.bin"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX) $(OBJCOPY_BIN)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
