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
Pruebas.elf \

SIZE_OUTPUT += \
default.size.stdout \

OBJDUMP_LIST += \
Pruebas.list \

OBJCOPY_HEX += \
Pruebas.hex \

OBJCOPY_BIN += \
Pruebas.bin \

OBJCOPY_VERILOG += \
Pruebas.verilog \


# All Target
all: Pruebas.elf secondary-outputs

# Tool invocations
Pruebas.elf: $(OBJS) $(USER_OBJS) D:\Projects\STM32F103RE\Pruebas\STM32F103RETX_FLASH.ld
	arm-none-eabi-gcc -o "Pruebas.elf" @"objects.list" $(USER_OBJS) $(LIBS) -mcpu=cortex-m3 -T"D:\Projects\STM32F103RE\Pruebas\STM32F103RETX_FLASH.ld" --specs=nosys.specs -Wl,-Map="Pruebas.map" -Wl,--gc-sections -static --specs=nano.specs -mfloat-abi=soft -mthumb -Wl,--start-group -lc -lm -Wl,--end-group
	@echo 'Finished building target: $@'
	@echo ' '

default.size.stdout: $(EXECUTABLES)
	arm-none-eabi-size  $(EXECUTABLES)
	@echo 'Finished building: $@'
	@echo ' '

Pruebas.list: $(EXECUTABLES)
	arm-none-eabi-objdump -h -S $(EXECUTABLES) > "Pruebas.list"
	@echo 'Finished building: $@'
	@echo ' '

Pruebas.hex: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O ihex $(EXECUTABLES) "Pruebas.hex"
	@echo 'Finished building: $@'
	@echo ' '

Pruebas.bin: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O binary $(EXECUTABLES) "Pruebas.bin"
	@echo 'Finished building: $@'
	@echo ' '

Pruebas.verilog: $(EXECUTABLES)
	arm-none-eabi-objcopy  -O verilog $(EXECUTABLES) "Pruebas.verilog"
	@echo 'Finished building: $@'
	@echo ' '

# Other Targets
clean:
	-$(RM) *
	-@echo ' '

secondary-outputs: $(SIZE_OUTPUT) $(OBJDUMP_LIST) $(OBJCOPY_HEX) $(OBJCOPY_BIN) $(OBJCOPY_VERILOG)

.PHONY: all clean dependents
.SECONDARY:

-include ../makefile.targets
