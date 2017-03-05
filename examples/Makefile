#
# Building Chisel examples without too much sbt/scala/... stuff
#
# sbt looks for default into a folder ./project and . for build.sdt and Build.scala
# sbt creates per default a ./target folder

# Make it work in Docker :)
showSuccess := false

SBT = sbt

# Force silence!
.SILENT:

# Generate Verilog code

all: alu knight uart

alu:
	@$(SBT) --silent "run-main simple.AluMain"

knight:
	@$(SBT) --silent "run-main simple.KnightMain"

uart:
	@$(SBT) --silent "run-main uart.SenderMain"


# Generate the C++ simulation and run the tests

test: alu-test knight-test fifo-test

alu-test:
	$(SBT) "run-main simple.AluTester"

counter:
	$(SBT) "run-main simple.CounterTester"

knight-test:
	$(SBT) "run-main simple.KnightTest"

fifo-test:
	$(SBT) "run-main simple.FifoTester"

fifo-view:
	gtkwave generated/BubbleFifo.vcd --save=bubble.gtkw

fifo: fifo-test fifo-view


